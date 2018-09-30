1.. Markdown에 관하여
============

1.1. Markdown이란?
--------
Markdown은 텍스트 기반의 마크업언어로 2004년 존그루버에 의해 만들어졌으며 쉽게 쓰고 읽을 수 있으며 HTML로 변환이 가능하다. 특수기호와 문자를 이용한 매우 간단한 구조의 문법을 사용하여 웹에서도 보다 빠르게 컨텐츠를 작성하고 보다 직관적으로 인식할 수 있다. 마크다운이 최근 각광받기 시작한 이유는 깃헙(https://github.com) 덕분이다. 깃헙의 저장소Repository에 관한 정보를 기록하는 README.md는 깃헙을 사용하는 사람이라면 누구나 가장 먼저 접하게 되는 마크다운 문서였다. 마크다운을 통해서 설치방법, 소스코드 설명, 이슈 등을 간단하게 기록하고 가독성을 높일 수 있다는 강점이 부각되면서 점점 여러 곳으로 퍼져가게 된다.

1.2. Markdown의 장-단점
--------

### 1.2.1. 장점
1. 간결하다.
2. 별도의 도구없이 작성가능하다.
3. 다양한 형태로 변환이 가능하다.
4. 텍스트(Text)로 저장되기 때문에 용량이 적어 보관이 용이하다.
5. 텍스트파일이기 때문에 버전관리시스템을 이용하여 변경이력을 관리할 수 있다.
6. 지원하는 프로그램과 플랫폼이 다양하다.

### 1.2.2. 단점
1. 표준이 없다.
2. 표준이 없기 때문에 도구에 따라서 변환방식이나 생성물이 다르다.
3. 모든 HTML 마크업을 대신하지 못한다.


2.. Markdown 사용법(문법)
============

2.1. 헤더(Headers)
--------

•큰제목: 문서 제목

This is an H1
=============



•작은제목: 문서 부제목

This is an H2
-------------



•글머리: 1~6까지만 지원

# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
####### This is a 7.

2.2. 강조(Emphasis)
--------

각각 `<em>, <strong>, <del>` 태그로 변환됩니다.

밑줄을 입력하고 싶다면 `<u></u>` 태그를 사용하세요.

이텔릭체는 *별표(asterisks)* 혹은 _언더바(underscore)_를 사용하세요.

두껍게는 **별표(asterisks)** 혹은 __언더바(underscore)__를 사용하세요.

**_이텔릭체_와 두껍게**를 같이 사용할 수 있습니다.

취소선은 ~~물결표시(tilde)~~를 사용하세요.

<u>밑줄</u>은 `<u></u>`를 사용하세요.



2.3. 목록(List)
--------

`<ol>, <ul>` 목록 태그로 변환됩니다.
1. 순서가 필요한 목록
  
1. 순서가 필요한 목록

  - 순서가 필요하지 않은 목록(서브)
  
  - 순서가 필요하지 않은 목록(서브)
  
1. 순서가 필요한 목록

  1. 순서가 필요한 목록(서브)
  
  1. 순서가 필요한 목록(서브)
  
1. 순서가 필요한 목록


- 순서가 필요하지 않은 목록에 사용 가능한 기호
  - 대쉬(hyphen)
  - 별표(asterisks)
  + 더하기(plus sign)


2.4. 링크(Links)
--------

`<a>`로 변환됩니다.
  
  
[GOOGLE](https://google.com)

[NAVER](https://naver.com "링크 설명(title)을 작성하세요.")

[상대적 참조](../users/login)

[Dribbble][Dribbble link]

[GitHub][1]

문서 안에서 [참조 링크]를 그대로 사용할 수도 있습니다.

다음과 같이 문서 내 일반 URL이나 꺾쇠 괄호(`< >`, Angle Brackets)안의 URL은 자동으로 링크를 사용합니다.
구글 홈페이지: https://google.com
네이버 홈페이지: <https://naver.com>

[Dribbble link]: https://dribbble.com
[1]: https://github.com
[참조 링크]: https://naver.com "네이버로 이동합니다!"


2.5. 이미지(Images)
--------

`<img>`로 변환됩니다.

링크과 비슷하지만 앞에 !가 붙습니다.

![대체 텍스트(alternative text)를 입력하세요!](http://www.gstatic.com/webp/gallery/5.jpg "링크 설명(title)을 작성하세요.")

![Kayak][logo]

[logo]: http://www.gstatic.com/webp/gallery/2.jpg "To go kayaking."


2.6. 이미지에 링크
--------

마크다운 이미지 코드를 링크 코드로 묶어 줍니다.

[![Vue](/images/vue.png)](https://kr.vuejs.org/)


2.7. 코드(Code) 강조
--------

`<pre>, <code>`로 변환됩니다.

숫자 1번 키 왼쪽에 있는 (Grave)를 입력하세요


2.8. 인라인(inline) 코드 강조
--------

`background`혹은 `background-image` 속성으로 요소에 배경 이미지를 삽입할 수 있습니다.


2.9. 블록(block) 코드 강조
--------

숫자 1번 키 왼쪽에 있는 (Grave)를 3번 이상 입력하고 코드 종류도 적습니다.

```html
<a href="https://www.google.co.kr/" target="_blank">GOOGLE</a>
```

```css
.list > li {
  position: absolute;
  top: 40px;
}
```

```javascript
function func() {
  var a = 'AAA';
  return a;
}
```

```bash
$ vim ./~zshrc
```

```python
s = "Python syntax highlighting"
print s
```

```
No language indicated, so no syntax highlighting. 
But let's throw in a tag.
```


2.10. 표(Table)
--------

`<table>` 태그로 변환됩니다.

헤더 셀을 구분할 때 3개 이상의 -(hyphen/dash) 기호가 필요합니다.

헤더 셀을 구분하면서 :(Colons) 기호로 셀(열/칸) 안에 내용을 정렬할 수 있습니다.

가장 좌측과 가장 우측에 있는 |(vertical bar) 기호는 생략 가능합니다.

| 값 | 의미 | 기본값 |
|---|:---:|---:|
| `static` | 유형(기준) 없음 / 배치 불가능 | `static` |
| `relative` | 요소 자신을 기준으로 배치 |  |
| `absolute` | 위치 상 부모(조상)요소를 기준으로 배치 |  |
| `fixed` | 브라우저 창을 기준으로 배치 |  |

값 | 의미 | 기본값
---|:---:|---:
`static` | 유형(기준) 없음 / 배치 불가능 | `static`
`relative` | 요소 **자신**을 기준으로 배치 |
`absolute` | 위치 상 **_부모_(조상)요소**를 기준으로 배치 |
`fixed` | **브라우저 창**을 기준으로 배치 |


2.11. 인용문(BlockQuote)
--------

`<blockquote>` 태그로 변환됩니다.

인용문(blockQuote)

> 남의 말이나 글에서 직접 또는 간접으로 따온 문장.
> _(네이버 국어 사전)_

BREAK!

> 인용문을 작성하세요!
>> 중첩된 인용문(nested blockquote)을 만들 수 있습니다.
>>> 중중첩된 인용문 1
>>> 중중첩된 인용문 2
>>> 중중첩된 인용문 3

2.12. 원시 HTML(Raw HTML)
--------

마크다운 문법이 아닌 원시 HTML 문법을 사용할 수 있습니다.

<u>마크다운에서 지원하지 않는 기능</u>을 사용할 때 유용하며 대부분 잘 동작합니다.

<img width="150" src="http://www.gstatic.com/webp/gallery/4.jpg" alt="Prunus" title="A Wild Cherry (Prunus avium) in flower">

![Prunus](http://www.gstatic.com/webp/gallery/4.jpg)


2.13. 수평선(Horizontal Rule)
--------

각 기호를 3개 이상 입력하세요.

---
(Hyphens)

***
(Asterisks)

___
(Underscores)


2.14. 줄바꿈(Line Breaks)
--------


동해물과 백두산이 마르고 닳도록 

하느님이 보우하사 우리나라 만세   <!--띄어쓰기 2번-->

무궁화 삼천리 화려 강산<br>

대한 사람 대한으로 길이 보전하세


일반 줄비꿈이 동작하지 않는 환경(설정 및 버전에 따라)의 경우, ‘2번의 띄어쓰기’나 <br>를 활용할 수 있습니다.
