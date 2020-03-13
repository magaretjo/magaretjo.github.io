---
title: "Github Pages 시작하기 4편"
last_modified_at: 2020-03-09T00:00:00-00:00
classes: single
categories:
  - github pages
  # 카테고리는 반드시 아래 예시 중에 골라 입력해주세요.
  # 예시에 원하는 카테고리가 없을 시, 예시에 추가해주시고 이 문서를 commit&push 해주세요.
  # ex)Cloud, AI, Big Data, Culture, Spring, MSA
  # Agile Categories : agile-overview, scrum-quickguide, agile-reference, agile-practices, agile-thingy
tags:
  - git
  - github
  - github pages
#	태그는 자유롭게 개수 제한 없이 입력할 수 있습니다. 아래는 예시입니다.
# ex)Cloud: k8s, Docker, CloudZ, Azure, AWS, Google Cloud
#	  AI: Abril, Tensor Flow
#   Big Data: accuinsight+, QUTA
#   Agile: agile, scrum, lean, jira, confluence, release plan, sprint plan, backlog, review, retrospective, scrum master, product owner, scrum team, dev team,
author: Judy
excerpt: "Github Pages 초기 사용자를 위한 가이드 4편입니다. (포스팅 작성에 필요한 Markdown 문법 배우기)"
toc: true 
toc_sticky: true 
toc_label: "List" 
---

이제 포스팅을 작성해볼 시간입니다. Github Pages는 기본적으로 Markdown 문서를 기반으로 합니다.

# Markdown 특징

Markdown은 배우기 쉽고 간편하며, 가볍다는 장점이 있습니다. 그리고 다양한 블로깅 플랫폼에서 Markdown문서를 지원하기 시작하면서 다른 플랫폼으로 옮기더라도 Markdown문서만 있으면 기존의 포스팅을 다시 작성할 필요없이 해당 문서들만 복사/붙여넣기 하면 된다는 장점이 있죠!
또, 특별한 형태의 에디터가 필요없다는 것도 어떻게 보면 큰 장점이 될 수도 있겠네요 :)

그럼 많고 많은 Markdown 문법 중 가장 많이 쓰이고 꼭 필요한 문법들 위주로 알려드리겠습니다.

# Markdown 문법

## 코드 줄바꿈

코드 줄바꿈은 라인 끝에 스페이스 공백을 2번 표기 또는 \\ (백슬래시) 2개를 붙인다.

-> 하지만 Visual Studio Code에서 Markdown All in One을 설치했기 때문에, **엔터를 두 번** 입력하면 줄바꿈이 됩니다.

```bash
기본적인 텍스트 표기 방식이다.
마크다운은 줄바꿈을 인식하지 않는다.
 
줄바꿈을 하기 위해서는 Enter를 두 번

입력한다.
```
![](https://engineering-skcc.github.io/assets/images/2020-03-09-17-08-55.png)


## Header 달기

제목을 붙이는 방법입니다.

#를 갯수에 맞게 붙여주고 한 칸을 띄어주는 것이 중요!
```
# This is a H1
## This is a H2
```

![](https://engineering-skcc.github.io/assets/images/2020-03-09-17-10-10.png)

![](https://engineering-skcc.github.io/assets/images/2020-03-09-17-10-36.png)

## 인용

참고자료 출처나 인용문구에 사용합니다.

```
> This is a blockqute.
```
![](https://engineering-skcc.github.io/assets/images/2020-03-09-17-11-44.png)

### 단계별 인용

```
> This is a first blockqute.
>> This is a second blockqute.
>>> This is a third blockqute.
```
![](https://engineering-skcc.github.io/assets/images/2020-03-09-17-12-16.png)

## 정렬 목록

```
1. 봄
2. 여름
3. 가을
4. 겨울
```
![](https://engineering-skcc.github.io/assets/images/2020-03-09-17-12-44.png)

## 비정렬 목록

Tab을 눌러 하위 정렬을 입력합니다.

```
- 과자
    -라면
        - 사탕
```
![](https://engineering-skcc.github.io/assets/images/2020-03-09-17-13-45.png)

## 코드 인용

```
function test() {
  console.log("notice the blank line before this function?");
}
```
![](https://engineering-skcc.github.io/assets/images/2020-03-09-17-14-16.png)

### 코드 인용 - 언어별 문법 하이라이트

ruby, python, java, c, sql등 다양한 언어를 지원합니다.
```
    ```cpp
    int main() {
    int y = SOME_MACRO_REFERENCE;
    int x = 5 + 6;
    cout << "Hello World! " << x << std::endl();
    }
    ```
```
![](https://engineering-skcc.github.io/assets/images/2020-03-09-17-14-49.png)

## 수평선(구분선)

아래 코드 모두 수평선(구분선)을 만드는 코드 입니다.
```
* * *
***
*****
- - -
---------------------------------------
```

* * *
***
*****
- - -
---------------------------------------

## 링크 삽입

```
- 링크 표시법 : [Title](link)
[Google 페이지 링크](https://google.com)
```

[Google 페이지 링크](https://google.com)

```
<https://google.com>
```

<https://google.com>

## 이미지 삽입

-> 이미지 캡쳐 후 Ctrl+C로 클립보드에 복사

-> 복사된 이미지를 Ctrl+Alt+V로 삽입이 가능하며 Path 및 Naming 또한 자동으로 설정됩니다. (MacOS : command+ option+ V)

또는 assets/images/ 폴더에 직접 이미지 파일 삽입 후, 해당 이미지 주소를 입력하세요

직접 삽입시 이미지 주소 : https://www.engineering-skcc.github.io/assets/images/filename

**filename**은 반드시 해당 file명으로 변경하셔야합니다.

```
![이미지 설명](이미지 주소)
```
### 이미지 정렬

```
![이미지 설명](이미지 주소){: .align-center}
```

-> align-left, align-right으로도 가능합니다.

### 이미지 사이즈 조정하기

```
<img src="이미지 주소" width="500">
```

-> width 를 바꿔서 사이즈 조정

#### 사이즈 조정한 이미지 가운데 정렬

```
<center><img src="이미지 주소" width="500"></center>
```

## 표 삽입

Markdown의 유일한 단점이라고 생각하는.. 표 삽입 입니다. 문법은 아래와 같습니다.

- | 파이프 라인으로 컬럼을 구분
- :-------로 헤더와 body를 구분해줌. (:----- → 왼쪽 정렬 , :------: → 가운데 정렬, -----: → 오른쪽 정렬)
- ---- 테이블 body간을 구분
- ====로 테이블 foot을 구분

```
| 헤더1 | 헤더2 | 헤더3 |
|:--------|:-------:|--------:|
| 컬럼1   | 컬럼2   | 컬럼3   |
| 컬럼4   | 컬럼5   | 컬럼6   |
|----
| 컬럼1   | 컬럼2   | 컬럼3   |
| 컬럼4   | 컬럼5   | 컬럼6   |
|=====
| Foot1   | Foot2   | Foot3
{: rules="groups"}
```
<br>


![](https://engineering-skcc.github.io/assets/images/2020-03-09-17-24-20.png)

하지만 개발자들은 복잡하고 어려운 것을 싫어하죠. 그래서 준비했습니다.

Markdown용 표를 만들어주는 사이트! -> [http://www.tablesgenerator.com/markdown_tables]

**한 셀에 여러 줄 입력 시 `Line breaks as <br>` 반드시 체크!!**

| 헤더1 | 헤더2 | 헤더3 |
|:--------|:-------|--------:|
| 컬럼1   | 컬럼2<br>- 구하기 타오르고 길지 만물은 있는 얼마나 것이다. 그들의 작고 눈에 행복스럽고 온갖 예가 낙원을 사막이다. 것은 그러므로 꽃이 이는 인도하겠다는 귀는 것이다.<br>- 곳이 인생에 인생에 사막이다. 우는 실로 밥을 이상은 더운지라 열락의 끓는다.<br>- 길을 그러므로 청춘 길지 싶이 말이다. 이상의 바로 평화스러운 황금시대를 인간이 사랑의 사막이다. 그것은 역사를 뜨고, 거친 인생에 피어나기 끝까지 구할 이것이다.   | 컬럼3   |
| 컬럼4   | <li>abcd<li>efghi Ddkjlalkjg of jlqoie jood<li>aga in The dkoudled beouajq.   | 컬럼6   |
|----
| 컬럼1   | 컬럼2   | 컬럼3   |
| 컬럼4   | 컬럼5   | 컬럼6   |
|=====
| Foot1   | •	Commitment (전념,확약) : 약속한 것을 확실이 이행/실현하는 것<br>•	Focus (집중) : 확약한 것의 실천을 위해 집중/최선을 다하는 것<br>•	Openness (개방성) : 어떤 것이 자신에게 불리해도 숨기지 않는 것<br>•	Respect (존중) : 자신과 다른 사람의 의견을 존중하는 것<br>•	Courage (용기) : 실패나 거부에 대한 두려움 없이 의사를 개진할 수 있도록 함
   | Foot3 |
{: rules="groups"}

## 각주

```
각주1 선언부분 a footnote[^1]. 
각주2 선언부분 a footnote[^2].
 
[^1]: 각주에 대한 설명 내용 부분 (문서 최하단)

```
![](https://engineering-skcc.github.io/assets/images/2020-03-09-17-26-16.png)

## 인라인 코드

문장 내에서 특정 문자를 escape 시켜줍니다.
`를 사용하고 싶다면
`text`를 ``2개 붙여 감싸줍니다.

```
문장내의 `###` 사용을 무시함
 
문장내의 `` `code` `` 사용을 무시함
```
![](https://engineering-skcc.github.io/assets/images/2020-03-09-17-27-34.png)

## Text 강조(Bold, Italic)

아래 Command 입력으로 사용하셔도 되고, 기본환경설정의 Extension을 모두 설치했다면 Ctrl+B로 Bold, Ctrl+I 로 Italic이 가능합니다. 

```
이것은 *이텔릭*, **진하게** 
이것도 _이텔릭_, __진하게__
```
![](https://engineering-skcc.github.io/assets/images/2020-03-09-17-28-18.png)

## 글씨 색 입히기

```html
<span style="color:red"> **: User user = userRepository.findById(id).orElseThrow(()->new UserNotFoundException("User not found"));** </span>
```
![](https://engineering-skcc.github.io/assets/images/2020-03-09-17-29-42.png)

## 버튼

링크 삽입이나 페이지, 홈에서 버튼을 만드는 방법입니다.

```html
<a href="#" class="btn btn--primary">Link Text</a>
```

|  Button Type  | Example |           Class          |                  Kramdown                 |
|:-------------:|:-------:|:------------------------:|:-----------------------------------------:|
|    Default    |   Text  | .btn                     | [Text](#link){: .btn}                     |
|    Primary    |   Text  | .btn .btn--primary       | [Text](#link){: .btn .btn--primary}       |
|    Success    |   Text  | .btn .btn--success       | [Text](#link){: .btn .btn--success}       |
|    Warning    |   Text  | .btn .btn--warning       | [Text](#link){: .btn .btn--warning}       |
|     Danger    |   Text  | .btn .btn--danger        | [Text](#link){: .btn .btn--danger}        |
|      Info     |   Text  | .btn .btn--info          | [Text](#link){: .btn .btn--info}          |
|    Inverse    |   Text  | .btn .btn--inverse       | [Text](#link){: .btn .btn--inverse}       |
| Light Outline |   Text  | .btn .btn--light-outline | [Text](#link){: .btn .btn--light-outline} |


| Button Type |     Example    |               Class              |                      Kramdown                     |
|:-----------:|:--------------:|:--------------------------------:|:-------------------------------------------------:|
| X-Large     | X-Large Button | .btn .btn--primary .btn--x-large | [Text](#link){: .btn .btn--primary .btn--x-large} |
| Large       | Large Button   | .btn .btn--primary .btn--large   | [Text](#link){: .btn .btn--primary .btn--large}   |
| Default     | Default Button | .btn .btn--primary               | [Text](#link){: .btn .btn--primary }              |
| Small       | Small Button   | .btn .btn--primary .btn--small   | [Text](#link){: .btn .btn--primary .btn--small}   |

## Notice블럭

| Notice Type | Class            |
|-------------|------------------|
| Default     | .notice          |
| Primary     | .notice--primary |
| Info        | .notice--info    |
| Warning     | .notice--warning |
| Success     | .notice--success |
| Danger      | .notice--danger  |

```
Notice 빨간박스 예제!
**Tips** 팁박스입니다.
{: .notice--danger}
```

Notice 빨간박스 예제!
**Tips** 팁박스입니다.
{: .notice--danger}


---

긴 Markdown 문법 여정이 끝났네요...

아마 포스팅 방법 관련해서 계속해서 찾게 될 글이 아닌가 싶네요!

유용하게 활용하시길 바랍니다 :)

위 내용 중 틀린 부분이 있거나 추가로 팁을 공유해주실 분은 댓글로 코멘트를 남겨주세요~! 

감사합니다!