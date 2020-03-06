---
title: "Jira는 무엇이고, 어떻게 시작하면 좋을까요?"
last_modified_at: 2020-02-24T00:00:00-00:00
classes: wide
categories:
  - culture
tags:
  - Agile
  - Jira
  - tool setting
author: jaehoon1104
excerpt: "Agile 프로젝트 운영을 위한 Tool인 Jira 세팅법에 관한 이야기입니다."
toc: true
toc_sticky: true
toc_label: "List"
---

## Jira는 무엇일까요?

Agile 프로젝트도 기존 프로젝트 같이 일감 및 일정관리를 위한 도구(Tool)가 필요합니다. 수평성과 투명성에 기반한 일감관리를 위한 툴로서 조호 스프린트(Zoho Sprints), 먼데이닷컴(Monday.com), 칸바나이즈(Kanbanize), 버그디거(BugDigger), 아사나(Asana), 지라(Jira) 등이 있습니다만, 이번 포스팅에서는 지라(Jira)라는 프로젝트 운영 관리 도구를 좀 더 자세히 살펴보겠습니다.
>>
<center><img src="https://engineering-skcc.github.io/assets/images/jira-software-logo.png" width="300"></center>

>>

지라(Jira)는 아틀라시안(Atlassian)이 개발한 애자일용 프로젝트 관리 프로그램으로, 이슈 추적, 버그 추적, 일감 관리 등으로 통한 전반적인 프로젝트 관리 소프트웨어입니다. 이름은 일본 애니로 잘 알려진 고지라(Godzilla) 에서 따왔다고 하네요. 아틀라시안이 호주 회사인 것으로 알고 있는데 그 곳에도 고지라 팬이 많나봅니다. ㅎㅎㅎ

>>

<center><img src="https://engineering-skcc.github.io/assets/images/godzilla.jpg" width="400"></center>

>>
>>

지라 소프트웨어는 아틀라시안 홈페이지에서 평가판을 무료로 다운 받을 수 있습니다.

<https://www.atlassian.com/ko/software/jira>

물론 사용자수에 따라 책정된 일정비용을 지불해야 모든 기능을 사용할 수 있습니다. 클라우드 버전, 서버 버전 중 선택하여 다운 받을 수 있고 필요에 따라 협업 및 문서, 코드 관리등을 위한 컨플루언스(Confluence), 빌드 및 배포 관리를 위한 뱀부(Bamboo), 사용자 관리를 위한 크라우드(Crowd)와 연계하여 사용할 수 있습니다.

>>
>>

## Jira 시작하기

그럼 지라(Jira) 세팅 및 운영방법을 간단하게 알아보도록 하죠. 천천히 따라하시면 큰 문제없이 쉽게 시작하실 수 있을겁니다.

- 우선 아래 URL에 접속합니다. 


     <https://www.atlassian.com/ko/software/jira>



- 위 URL에 접속하면 아래와 같은 화면이 나오고 여기서 [무료 평가판 사용] 버튼을 누릅니다.

<center><img src="https://engineering-skcc.github.io/assets/images/지라1.png" width="500"></center>


- 이제 Jira Software 클라우드에서 체험하기를 클릭하면,

<center><img src="https://engineering-skcc.github.io/assets/images/지라2.png" width="500"></center>


- 계정을 만드는 화면이 나옵니다. 구글 메일이나 자신이 사용하는 이메일로 가입하시면 됩니다.

<center><img src="https://engineering-skcc.github.io/assets/images/지라3.png" width="500"></center>


- 가입을 마쳤으면 이제 계정(Account)를 생성합니다.

<center><img src="https://engineering-skcc.github.io/assets/images/지라4.png" width="500"></center>


- 계정을 생성했으면 원하는 사람을 초대해 멤버로 등록할 수 있고, 우리가 만들려고 하는 '프로젝트'를 만들고 나서도 얼마든지 등록할 수 있습니다. 다만, 평가판에서는 10명까지로 제한되어 있고 정식 버전에서는 사람 수에 따라 지불해야 하는 금액이 달라집니다.

<center><img src="https://engineering-skcc.github.io/assets/images/지라5.png" width="500"></center>


- 자, 다음으로 간단한 자기소개(개인설정)를 선택해 주시고

<center><img src="https://engineering-skcc.github.io/assets/images/지라6.png" width="500"></center>


- 지라에서 제공하는 클래식 템플릿 중 하나를 선택하게 됩니다. 우리는 이들 중 '스크럼(Scrum)'을 선택하겠습니다. 선택한 후에는 [만들기] 버트을 눌러주세요.

<center><img src="https://engineering-skcc.github.io/assets/images/지라7.png" width="500"></center>


- 스크럼을 만들었다면 우리가 일할 '프로젝트'를 만들어야 겠죠? 개념적으로 따지자면 프로젝트는 앞으로 진행하려는 일감들의 집합이라고 볼 수 있고, 스크럼은 그 프로젝트를 운영해 나갈 방식을 의미합니다. 

- 여기서 프로젝트명과 키는 여러분이 자유롭게 입력할 수 있습니다. 진행하고자 하는 일감을 대표할 수 있는 단어로 지정해 주세요. 저는 이번 포스팅을 위한 'SKJira가이드만들기'라는 이름으로 프로젝트명을 정했습니다.

<center><img src="https://engineering-skcc.github.io/assets/images/지라8.png" width="500"></center>


지금까지 지라(Jira)를 어떻게 시작해야 하는지에 대해 알아보았습니다. 간단하죠? 

<center><img src="https://engineering-skcc.github.io/assets/images/참쉽죠.jpg" width="500"></center>


아래부터는 지금까지의 과정을 거쳐 만들어 놓은 프로젝트에 우리가 할 일을 어떻게 설정하고 그것들을 어떻게 진행해야 하는지에 대해 알아보겠습니다.

>>
>>

## Jira 초기 세팅하기

자, 이제 프로젝트 안에 우리의 일감을 만들어 넣어볼까요? 'Jira 시작하기' 부분처럼 천천히 함께 해봅시다.


- 앞 선 과정에 따라 프로젝트를 만들고 나면 아래 그림과 같이 해당 프로젝트명이 왼편에 나오고 오른편에는 '활성 스프린트' 화면이 만들어 집니다.

<center><img src="https://engineering-skcc.github.io/assets/images/지라9.png" width="500"></center>


- 왼편 프로젝트 정보창에서 '백로그' 버튼을 클릭하시면 아래와 같은 화면이 나옵니다. 여기서 우리가 하려는 일들을 등록하려고 하는데 지라(Jira) 에서는 이런 일감을 '이슈'라고 칭합니다. 우리가 아는 '문제 혹은 위기상황'인 이슈와는 조금 다른 의미입니다. 말그대로 우리가 해결해야하는 일감을 '이슈'라고 하므로 혼동하지 않도록 주의해야 합니다.

- 아래 그림과 같이 '이슈 생성하기' 라고 쓰인 부분의 왼편에 있는 아이콘 버튼을 클릭합니다. 이 버튼을 클릭하면 그림과 같이 [스토리], [작업], [버그] 이렇게 세 선택박스가 나옵니다. 여기서 스토리는 위에 설명했듯 우리의 일감을 의미하고, 작업은 스토리의 세부업무라고 생각하면 쉽습니다. 그리고 버그는 말그대로 테스트 과정에서 도출되는 오류사항들입니다. 

- 참고로 [에픽] 이라는 스토리보다 상위의 개념도 있습니다. 간단하게는 스토리들의 모음 즉, 마일스톤 개념으로 이해해 주시면 됩니다. 에픽과 스토리, 작업 간의 관계를 설명하기에는 본 포스팅이 길어질 수 있으므로 이에 관한 사항은 추가 포스팅을 통해 추후 좀 더 자세히 살펴보겠습니다.

- 이제 스토리를 선택하고 바로 옆 칸에 우리 작업의 이름을 입력합니다. 스토리의 이름 혹은 일감의 이름을 정하는 건데, 어떤 일감인지를 잘 표현해 주는 단어 혹은 어구로 표현하는 것이 좋습니다. 팀원들이 공유하면서 어떤 일감인지 이해해야하기 때문이죠.

<center><img src="https://engineering-skcc.github.io/assets/images/지라10.png" width="500"></center>


- 이렇게 스토리들을 작성하면 자동적으로 스토리에는 자동적으로 아이디가 붙게되고 이 값은 unique한 값입니다. 스토리에 고유한 아이디가 붙는 이유는 각 스토리의 내역(History)를 쌓아 추적할 수 있도록 하기 위함이며, 이 내역는 향후 투명한 일감관리(진행상태 확인, 임의삭제 방지 등)를 위해 필수적인 요소입니다.

- 백로그 내 스토리는 무제한 만들 수 있으며, 스토리가 3개 이상 쌓이게 되면 '스프린트'를 만들 수 있습니다. 스프린트는 1주~4주 사이의 기간을 지정하여 일정 갯수의 스토리를 진행하는 애자일 일정 단위로 볼 수 있으며 추후 별도의 포스팅을 통해 자세히 설명하도록 하겠습니다.

<center><img src="https://engineering-skcc.github.io/assets/images/지라11.png" width="500"></center>

<center><img src="https://engineering-skcc.github.io/assets/images/지라12.png" width="500"></center>

- 스프린트를 만들면 처음엔 비어 있는 것을 확인 하실 수 있습니다. 새로 만들어진 스프린트 아래에 기존에 만들어 놓은 백로그에 스토리들이 쌓여 있는데 각 스토리는 'Drag&Drop' 방식으로 위의 스프린트로 옮겨 놓을 수 있습니다. 이렇게 옮긴 스토리는 해당 스프린트에 소속되어 해당 일정에 따라 수행되어야 합니다.

<center><img src="https://engineering-skcc.github.io/assets/images/지라13.png" width="500"></center>


- 위의 설명과 같이 하나 이상의 스토리가 옮겨지면 그 스프린트를 시작할 수 있습니다.

<center><img src="https://engineering-skcc.github.io/assets/images/지라14.png" width="500"></center>

<center><img src="https://engineering-skcc.github.io/assets/images/지라15.png" width="500"></center>


- 번외적인 설명입니다만, 스토리 이름을 클릭하면 화면 우측에 그림과 같이 상세정보가 표출되며 각 항목은 더블클릭을 통해 수정할 수 있습니다. 이는 백로그 상의 스토리도 마찬가지입니다. 또한 스토리명을 더블클릭하면 팝업화면을 통해 상세정보가 표출됩니다. 

<center><img src="https://engineering-skcc.github.io/assets/images/지라16.png" width="500"></center>


- 스프린트를 시작하면 아래 그림과 같이 '스프린트 시작'에 관한 정보를 지정할 수 있습니다.

    1. 우선 스프린트 이름을 지정할 수 있습니다. 저는 'JIRAGUID1 스프린트'로 지정했습니다.
    2. 다음으로 스프린트 기간을 지정할 수 있습니다. 1주에서 4주 사이의 기간을 지정하거나, 사용자가 지정할 수 있습니다.
    3. 세번째로 시작일과 시간을 지정할 수 있고, 위에 지정했던 기간을 더해 종료일을 자동으로 세팅합니다.
    4. 마지막으로 간단한 스프린트 목표를 작성할 수 있습니다.


<center><img src="https://engineering-skcc.github.io/assets/images/지라17.png" width="500"></center>



- 스프린트를 시작하면 아래와 같이 할일(To-do) 레인에 좀 전에 스프린트로 옮겨 놓은 스토리들을 확인할 수 있습니다. 이 때 할일(To-do), 진행중(In Progress), 완료(Done)과 같은 것을 '상태(Status)'라 일컫습니다.

- 본 포스팅에서 설명하는 지라 평가판은 앞선 3개의 상태만이 표시되지만, 정식 버전에서는 해결(Resolved),  종료(Closed), 취소(Cancel) 등의 상태를 추가하여 보다 다단한 단계를 설정해 좀 더 세밀한 관리가 가능합니다. 이에 관한 상세한 사항은 추후 포스팅을 통해 설명하도록 하겠습니다.

<center><img src="https://engineering-skcc.github.io/assets/images/지라18.png" width="500"></center>


- 할일(To-do) 레인에 있는 스토리는 Drag&Drop 방식으로 진행중(In Progress) 상태로 옮겨 일감이 시작됐음을 표시할 수 있습니다. 마찬가지로 진행중(In Progress) 상태의 스토리를 마무리했을 경우 완료(Done) 상태로 옮겨 일감을 마쳤음을 나타낼 수 있습니다.

<center><img src="https://engineering-skcc.github.io/assets/images/지라19.png" width="500"></center>

<center><img src="https://engineering-skcc.github.io/assets/images/지라20.png" width="500"></center>

<center><img src="https://engineering-skcc.github.io/assets/images/지라21.png" width="500"></center>


- 스프린트 내 모든 스토리가 완료(Done) 상태에 오게되면 스프린트를 완료할 수 있습니다.

<center><img src="https://engineering-skcc.github.io/assets/images/지라22.png" width="500"></center>

<center><img src="https://engineering-skcc.github.io/assets/images/지라23.png" width="500"></center>


- 스프린트를 완료하게 되면 해당 스프린트 진행에 대한 보고서가 나오고 화면 아래 쪽에서 완료된 스토리 목록을 확인할 수 있습니다.

<center><img src="https://engineering-skcc.github.io/assets/images/지라24.png" width="500"></center>


지금까지 Jira는 무엇이고 어떻게 시작해야하는지, 그리고 어떻게 스토리(이슈)를 작성하여 스프린트를 진행하는지에 대한 사항을 알아보았습니다. 향후에는 스프린트와 스토리의 상태에 관한 사항을 조금 더 자세하게 다룰 예정이니 기대해 주세요. 그리고!!! 포스팅 내용 중 오류가 있거나 수정되어야 하는 부분이 있다면 댓글로 언제든지 알려주시면 감사하겠습니다~^^


>출처: CIO.com 및 Atlassian 홈페이지
