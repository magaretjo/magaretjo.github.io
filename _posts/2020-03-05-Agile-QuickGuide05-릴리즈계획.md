---
title: "Agile 프로젝트 퀵가이드(5)-릴리즈 계획 수립"
last_modified_at: 2020-03-05T16:00:00-30:00
classes: wide
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
## <span class="mg_title_1">제품 백로그(Product Backlog)란?
  
보통 Release라 함은 배포를 의미한다. 스크럼 프레임워크에서 Release Plan은 단순 배포가 아닌 시장 또는 고객이 사용하는 Production 환경으로 출시하는 것을 말한다. 
출시 계획은 고객가치 / 전반적인 품질 / 범위 / 일정 / 에산 사이에서 균형을 이루어 결정하도록 한다. 제품 출시는 시장 상황이나 TTM(Time-To-Market)을 고려하여 수차례에 걸쳐 이루어질 수도 있다.
또한 Release Plan은 매 스프린트 수행 도중에, 수정될 수 있다. 스프린트에서 예상보다 빨리 제품을 구현하였다면 출시 일정을 앞당길 수도 있을 것이다. 이는 반대의 이야기도 성립된다.

**우선순위 선정 방법**

MoSCoW Rule에 따라 백로그 항목별로 우선순위를 부여하여, 제품 로드맵을 정의한다.
-	필수(Must-have) : 시스템에 반드시 필요하다.
-	희망(Should-have) : 중요하지만, 단기적으로는 차선책이 있다.
-	선택(Could-have) : 시간이 부족하다면 다음 릴리즈로 넘겨도 큰 문제가 없다.
-	보류(Won't-have) : 좋기는 하지만 미뤄도 전혀 문제가 없다.

![](/assets/images/agile/agile-backlog-moscow.png)
<br> 

**제품 로드맵 작성** 

제품 우선 순위에 따라 개발 스프린트에 대략적으로 할당하여 전체 로드맵을 수립한다.
![](/assets/images/aigle-product-roadmap.png) 


##	<span style="mg_title_1">스프린트 정의와 매핑 
스프린트는 스크럼의 핵심으로, 2~4주의 정해진 시간 동안 계획한 기능들을 “완료”하여 사용할 수 있고 출시 가능한 “제품 증분”으로 만들어 내는 Cycle을 의미한다.

프로젝트의 특성에 맞는 스프린트 “주기와 일정”을 정의하고 (전체 차수는 주기에 따라 결정) 각 스프린트 차수별로 주요 활동과 목표를 정의하도록 한다. 
다음은 스프린트별 목표 정의의 예시이다.<br>
![](/assets/images/agile/agile-sprint-goal.png){: width="500"} 
 <br>

스프린트의 목표가 정해지면 각 스프린트 동안 해야 할 백로그를 개략 선정하는데, 이를 “스프린트 매핑”이라 한다. 릴리즈 계획 수립 단계에서의 백로그 선정은 어디까지나 계획을 위한 후보 일감의 선정이며 확정은 아니다. 스프린트에 할당하는 일감은 매 스프린트 계획시 확정되는 것임을 다시 한번 강조한다. 

스프린트 계획에서 백로그 선정이 확정되더라도 릴리즈 계획 수립시에 이와 같은 매핑 작업을 하는 것은 전반적인 제품 출시 계획을 이해하고, 스크럼 팀간 개발 내용의 의존성을 해결하는 데에 도움을 줄 것이다. 고객가치에 우선하는 제품을 먼저 개발한다고 하여 작업 순서상의 선-후 관계를 무시해서는 안된다. 


- **통합테스트는 언제 하나**
  -	보통 품질을 높이기 위한 방법으로 통합테스트를 수행한다. 스크럼 프레임워크에서는 스프린트마다 완료된 추가 기능을 테스트하고 하나의 제품으로 지속적인 통합을 가이드하고 있으므로 통합테스트 기간을 따로 두지 않는다. 
  -	그러나 소규모의 작은 프로젝트가 아니거나, End-User가 별도로 존재한다거나, 무엇보다 출시 제품의 품질을 높이고, 생명과 안전에 직결된 완벽한 제품을 인도하기 위해서라면 통합테스트 기간을 따로 떼어놓아야 할 것이다. 
  -	위와 같은 상황이 아니더라도 우리나라의 SI 프로젝트 여건상 보통 통합테스트와 인수테스트를 끝내고 이행하는 게 바람직할 것이다.
{: .notice--memo}

<br>
릴리즈 계획이 수립되고 나면 다음과 같이 프로젝트 전체 일정표를 작성하여 프로젝트 관계자와 공유하도록 하자.
![](/assets/images/agile/agile-release-plan.png){: width="900"}


- **제품 백로그는 언제 변경할 수 있는가 ?**
   - 제품 백로그의 변경은 주로 스프린트 리뷰 및 스프린트 계획 미팅에서 논의하도록 한다.
   - 스프린트 도중에 변경이 되어야 한다면 스프린트 계획 미팅시 이에 대해 충분히 검토되지 않았음을 의미한다. 보다 상세한 내용은 스프린트 계획 편에서 다루도록 하겠다. 
{: .notice--memo} 


***

<div class="mg_subject_1"><b>Related Posts : </b></div> 
<div class="mg_content_1">
<a href="/agile-quickguide/Agile-QuickGuide04-제품백로그도출/">QuickGuide 04</a> > 제품 백로그 도출 <br>
<a href="/agile-quickguide/Agile-QuickGuide06-소통&품질/">QuickGuide 06</a> > 의사소통 및 품질 계획 
</div>
<br>

< EOF >