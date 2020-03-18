---
title: "Agile 프로젝트 Starting 퀵가이드-Appendix.JIRA환경설정"
last_modified_at: 2020-03-06T16:00:00-30:00
classes: single
categories:
  - agile-quickguide
  # 카테고리는 반드시 아래 예시 중에 골라 입력해주세요.
  # 예시에 원하는 카테고리가 없을 시, 예시에 추가해주시고 이 문서를 commit&push 해주세요.
  # ex)Cloud, AI, Big Data, Culture, Spring, MSA
tags:
  - agile
  - scrum
  - project
  - release
  - milestone
#	태그는 자유롭게 개수 제한 없이 입력할 수 있습니다. 아래는 예시입니다.
# ex)Cloud: k8s, Docker, CloudZ, Azure, AWS, Google Cloud
#	  AI: Abril, Tensor Flow
#   Big Data: accuinsight+, QUTA
author: magaretjo
excerpt: "릴리즈 계획은 무엇이며, 무엇을 릴리즈할 것인가?"
toc: true #(toc를 사용하지 않을 경우에만 false로 변경)
toc_sticky: true #(toc를 사용하지 않을 경우에만 false로 변경)
toc_label: "List" #(toc 사용시-변경x, 사용하지 않을 시 삭제)
---
<br>
## <span class="mg_title_1">스크럼 프로젝트의 관리 지표

### JIRA시스템 용어

<table class="mj_table">
<thead>
  <tr><th>용어</th><th>설명</th>
  </tr>
</thead>
<tbody>
  <tr><td class="mj_col1">•	Project</td>
      <td>- 일감(Issue)를 관리하는 최상위 카테고리</td>
  </tr>
  <tr><td class="mj_col1">•	일감(Issue)</td>
      <td><p>- JIRA에서는 Project의 백로그 관리를 위한 스토리(Story), 새로운 기능, Bug, 개선사항 등 다양한 형태의 작업들을 통틀어 일감 또는 Issue라고 호칭한다. </p>
          <p>- 일반적으로 말하는 Risk/Issue의 그 Issue와는 다르며, JIRA에서는 제품 백로그 Issue를 말하는 것이다.</p>
  </td>
  </tr>
  <tr><td class="mj_col1">•	상태(Status)</td>
      <td><p>- 일감(Issue)의 상태를 표시하는 기능</p>
          <p>- 보통 열림 / 진행중 / 해결 / 완료 등의 상태를 가지며, 다양한 상태값으로 커스터마이징이 가능하다.</p>
  </td>
  </tr>
  <tr><td class="mj_col1">•	흐름(Workflow)</td>
      <td>- 일감(Issue)이 진행되면서 상태가 전이(Transition)되는 전체 경로 </td>
  </tr>
  <tr><td class="mj_col1">•	필터(Filter)</td>
      <td>- 등록된 일감(Issue)를 조건에 맞게 검색하거나 데이터셋처럼 가져오는 기능</td>
  </tr>
  <tr><td class="mj_col1">•	보드(Borad)</td>
      <td><p>- 스크럼 or 칸반 방식에 맞게 일감의 상태 및 흐름을 한 눈에 보고, 일감 상태를 Update할 수 있는 작업 공간 </p>
         <p>- 스크럼 보드, 칸반 보드 등이 있다.</p>
  </td>
  </tr>
  <tr><td class="mj_col1">•	대시보드(Dashboard)</td>
      <td>-	가젯(Gaget)을 사용하여 프로젝트 진행상황에 대한 모니터링 및 통계 수치를 보고할 수 있는 화면
  </td>
  </tr>
</tbody>
</table>


### JIRA시스템의 일감구조
JIRA 에서는 프로젝트별 일감 관리를 위해 다음의 계층형 구조를 가지고 있다.
JIRA Admin 영역은 JIRA Administrator가 관리하는 영역이다. 프로젝트 공간을 관리하고 프로젝트의 유형 및 필수 속성을 관리한다. 

프로젝트 공간이 생성되고 관리자가 할당되면, 해당 관리자는 위의 Level 1~ Level 4에 해당하는 구조로 프로젝트의 일감을 관리할 수 있다.

![](/assets/images/agile/agile-jira-issue-structure.png) 

**구성요소**는 각각 전체 백로그를 시스템의 구성 단위 또는 모듈 단위로 구분하고자 할 경우에 사용한다. 구성요소 밑에 큰틀(에픽) 및 이야기, 작업 등을 등록하게 되면 해당 단위별로 검색 조건을 만들거나, 대시보드 모니터링, 통계 데이터 추출이 가능하다.

릴리즈 계획 수립시, 버전별로 출시 기능이 다른 경우에 **버전**을 등록하도록 한다. 버전별로 출시되기 위해 필요한 스토리 및 작업 등을 조회할 수 있는데, 만약 버전별로 MECE하게 기능이 나누어지지 않는다면 굳이 사용할 필요가 없다. 

Level 2 ~ 4까지가 실제적인 일감을 관리할 수 있는 유형들인데, 그림과 같이 Hierarchy 구조를 이룬다. 각 일감 유형에 대해서는 아래에서 설명한다.


### JIRA 일감 유형 
<table class="mj_table">
<thead>
  <tr><th>용어</th><th>설명</th>
  </tr>
</thead>
<tbody>
  <tr><td class="mj_col1">•	큰틀 (Epic)</td>
      <td><p>- 큰 단위의 기능 이름을 적어 놓은 것 또는 백로그를 묶기 위한 그룹명. </p>
          <p>- 따라서, 우선 순위도나 크기를 가질 수 없으며 Virtual로만 존재한다. </p>
      </td>
  </tr>
  <tr><td class="mj_col1">•	이야기 (Story)</td>
      <td><p>- 사용자 스토리를 일컬음. 기능 위주의 백로그를 이 유형에 등록한다.</p>
      </td>
  </tr>
  <tr><td class="mj_col1">•	작업 (Task)</td>
      <td><p>- 기능 외에 해야 할 작업. 즉, 비기능 위주의 백로그를 말함</p>
      </td>
  </tr>
  <tr><td class="mj_col1">•	버그(Bug)</td>
      <td><p>- 일반적으로 우리가 생각하는 기능 오류가 발생했을 때, 오류 수정에 대한 추가 공수가 발생하거나 일련의 절차가 필요하다면 그에 대한 일감 관리를 위해 “버그” 유형을 사용한다.</p>
          <p>- 사용자 리뷰 또는 테스트에서 발생하는 일감을 버그로 관리할 수 있다.</p>
          <p>- JIRA의 일감간 연결(link) 기능을 이용하여 어떤 스토리 또는 작업과 관계 있는 것인지도 추적 가능하다.</p>
      </td>
  </tr>
  <tr><td class="mj_col1">•	부작업 (Sub-task)</td>
      <td><p>- 이야기, 작업, 버그 등을 일감을 수행하기 위해 세부적인 일로 나뉘거나 여러 사람이 공동작업해야 하는 경우, 사용한다.</p>
          <p>- 상위의 이야기/작업/버그 유형에 종속이 되므로, 부작업의 완료는 어느 하나의 기능이 완성되었다고 보기 어렵다. 즉, 모든 부작업이 완료가 되어야 상위의 일감이 리뷰 가능한 형태의 완료로 간주된다.</p>
          <p>- 따라서 JIRA 대시보드 에서 몇몇 가젯은 상위의 일감에 대해서만 진행율을 계산한다.</p>
      </td>
  </tr>
</tbody>
</table>
<br>
이외에도 JIRA는 모든 항목과 속성을 메타로 관리하기 때문에 프로젝트별로 자유롭게 일감유형에 대한 커스터마이징이 가능하지만, 프로젝트별로 고유한 일감 유형을 생성할 경우 타 프로젝트와의 일관성 문제 및 JIRA Administrator의 운영 부담이 커지기 때문에 가능하다면 전사 차원의 가이드에 따른 일감 유형을 사용하는 것이 좋다.

당사 JIRA시스템은 다음과 같은 매우 기본적인 일감유형만을 사용할 수 있으므로, 아쉬운 점이 있기는 하지만 대부분의 프로젝트의 일감관리는 이정도 유형으로 충분히 커버가 가능하다.
<br>

## <span class="mg_title_1">스크럼보드 만들기


###	워크플로우 정의
JIRA에서 워크플로우(Workflw)는 일감이 진행되면서 변화되는 상태의 흐름을 말한다. 

최초에 일감이 등록되면 Open 상태가 될 것이고, 담당자가 해당 업무를 착수하게 되면 In Progress 상태가 될 것이다. 담당자가 어느 정도 일 마무리를 하고 나서 Resolved 상태로 바꾸어 주고, 이 일감에 대한 보고자 또는 제품 책임자와 같은 Approver가 검토한 후 완료 조건을 충족하면 Done 상태로 바꾸는 식으로 워크플로우를 정의할 수 있다.
![](/assets/images/agile/agile-jira-workflow1.png)

또는 다음과 같이 Review 상태를 추가할 수도 있다. 
![](/assets/images/agile/agile-jira-workflow2.png)

권한이 있는 경우 JIRA 프로젝트 설정 메뉴를 통해 워크플로우를 정의할 수 있는데, 위와 같이 기본적으로 제시되는 기본 워크플로우를 그대로 사용하기 바란다. 애지간한 JIRA Admin 또는 Devops 엔지니어가 아니라면 워크플로우를 잘못 정의했다가 흐름이 꼬일 수도 있으며, 일감의 상태 변경에 대한 권한도 함께 정의해주어야 하므로 매우 난이도가 높다.

또한 워크플로우가 복잡할수록 해당 일감이 완료 상태에 도달하기까지 그만큼 많은 상태를 전이(transition)시켜야 하는 셈이므로 일감 완료가 쉽지 않다. 당사의 JIRA 시스템은 JIRA Admin만 워크플로우를 정의할 수 있도록 되어 있으며, 스크럼 보드를 위한 유형은 단 2가지만 존재한다. 

따라서, 당사 JIRA 시스템을 이용할 경우에는 기본 유형의 워크플로우를 확인해 보는 정도로 만족하시라.
자체 시스템을 구축하고, JIRA 프로젝트 공간 관리자가 워크플로우 정의 권한이 있다면 새로운 유형의 워크플로우를 정의에 도전해 보는 것도 유익한 경험이 될 것이다. 

단, 한번 정의한 워크플로우는 변경이 거의 불가능하므로 일감 흐름에 대해 프로젝트 이해관계자와 사전 협의를 거쳐 등록하기 바란다.  

###	보드 설정하기
“보드”는 프로젝트를 관리하기 위해 실제 보여지는 공간을 말한다. 
대표적인 보드 유형으로는 스크럼보드와 칸반보드가 있고, 어떤 것을 선택하느냐에 따라 보드의 구성이 – 즉 화면에 보여지는 내용 - 이 바뀐다.  Agile 프로젝트이므로 스크럼보드를 선택하여 생성하도록 하자.
  
![](/assets/images/agile/agile-jira-board-create.png){: width="300"} ![](/assets/images/agile/agile-jira-board-type.png) 

보드 설정을 눌러, 보드에서 나타나게 되는 열(Column) 구성을 워크플로우에 맞게 재구성할 수 있다.
다음과 같이 가장 많이 쓰이는 형태의 열 목록을 구성해보자.
 

보드가 생성되고 나면 왼쪽 사이드메뉴에 “작업중인 스프린트” 메뉴가 생기게 된다. 이 메뉴는 현재 진행중 상태의 스프린트를 위한 화면을 보여준다. 즉, 해당 스프린트에 할당된 일감에 대해서 관리할 수 있도록 구성된 화면이 나타나는데, 앞서 설정한 열 구성에 맞게 보여지게 된다.
 

하지만 지금은 해당 메뉴에 들어가서 보면 화면에는 아무것도 나오지 않을 것이다. 아직 아무 일감도 스프린트도 등록되어 있지 않은 상태이기 때문이다.

이제 일감을 등록해보도록 하자. 


<br>

## <span class="mg_title_1">JIRA 프로젝트의 일감 정의하기

### 프로젝트 “구성요소” 정의

### 프로젝트 “일감” 등록

### 프로젝트 “스프린트” 생성 

### 스프린트별 일감 할당


<br>
## <span class="mg_title_1">대시보드 만들기

### 데이터 필터 정의

### 가젯 구성

***

<div class="mg_subject_1"><b>Related Posts : </b></div> 
<div class="mg_content_1">
<a href="/agile-quickguide/Agile-QuickGuide08-스크럼환경/">QuickGuide 08</a> > 스크럼환경 구성 
</div>
<br>


< EOF >