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



---------------------------------------------------------------------------------------------------------------------

git 명령어 정리
============

한동안 포스팅 주제도 못 잡았고 회사일이 너무 바빠서 블로그 엄두도 못 내다가 추석 연휴 때 고향에 내려가서 휴식을 취하며 독서도 하고 포스팅도 하려고 했지만.. 그것도 여의치 않았다. 대신 어떤 주제에 대해서 포스팅할지 고민은 하였는데 그중에 하나가 Git이다.

제목에 말머리 형태로 Git이라는 키워드를 달았는데 앞으로 포스팅 제목에 저런 식으로 말머리는 다는 것은 시리즈 형태의 포스팅을 의미한다고 보면 될 것이다. Git뿐 아니라 HTTP 등 다양한 주제로 포스팅을 할 생각이며 시간이 조금 걸리더라도 유용한 정보를 전달할 수 있도록 노력할 생각이다.

우선은 맛보기로 Git의 명령어에 대해서 정리해볼까 한다. 대부분의 사용자들이 주로 add, commit, push, pull, fetch 등을 사용하겠지만 Git의 명령어는 정말 다양하고 옵션도 많다. 이 포스팅에서는 간단하게 살펴보고 Git에 대해서 포스팅을 진행하면서 각 명령어가 쓰이는 곳과 더 상세한 설명을 추가하도록 하겠다.

참고로 아래 명령어를 보면 (-)대시 사이에 공백이 있는 걸 볼 수 있는데 Medium에서 대시를 이어서 쓸 수가 없다 보니 중간에 공백을 끼워 넣었다. 실제로 사용할 때는 (-)대시 사이에 공백 없이 이어서 써야 한다.


1.. 설정과 초기화
----------
> 전역 사용자명/이메일 구성하기
>### git config - -global user.name “Your name”
>### git config - -global user.email “Your email address”

> 저장소별 사용자명/이메일 구성하기(해당 저장소 디렉터리로 이동후)
>### git config user.name “Your name”
>### git config user.email “Your email address”

참고로 user 설정이 되어 있지 않으면 Github에 있는 repository에 변경사항을 푸시 한다고 해도 commit count 집계도 안되고 해당 커밋의 작성자 프로필 아이콘도 ? 로 표시되기 때문에 웬만하면 name과 email 주소를 설정하길 추천한다.

> 전역 설정 정보 조회
>### git config - -global - -list

> 저장소별 설정 정보 조회
>### git config - -list

> Git의 출력결과 색상 활성화하기
>### git config - -global color.ui “auto”

> 새로운 저장소 초기화하기
>### mkdir /path/newDir
>### cd /path/newDir
>### git init

> 저장소 복제하기
>### git clone <저장소 url>

> 새로운 원격 저장소 추가하기
>### git remote add <원격 저장소> <저장소 url>


2.. 기본적인 사용법
----------
> 아래 명령어에서 [ ]는 선택적인 매개변수를 의미한다.

> 새로운 파일을 추가하거나 존재하는 파일 스테이징하고 커밋하기
>### git add <파일>
>### git commit -m “<메시지>”

> 파일의 일부를 스테이징하기
>### git add -p [<파일> [<파일> [기타 파일들…]]]

> add 명령에서 Git 대화 모드를 사용하여 파일 추가하기
>### git add -i

> 수정되고 추적도되는 파일의 변경 사항 스테이징하기
>### git add -u [<경로> [<경로>]]

> 수정되고 추적되는 모들 파일의 변경 사항 커밋하기
>### git commit -m “<메시지>” -a

> 작업트리의변경 사항 돌려놓기
>### git checkout HEAD <파일> [<파일>]

> 커밋되지 않고 스테이징된 변경 사항 재설정하기
>### git reset HEAD <파일> [<파일>]

> 마지막 커밋 고치기
>### git commit -m “<메시지>” - -amend

> 이전 커밋을 수정하고 커밋 메시지를 재사용하기
>### git commit -C HEAD - -amend


3.. 브랜치
----------
> 지역 브랜치 목록 보기
>### git branch

> 원격 브랜치 목록 보기
>### git branch -r

> 지역과 원격을 포함한 모든 브랜치 목록 보기
>### git branch -a

> 현재 브랜치에서 새로운 브랜치 생성하기
>### git branch <새로운 브랜치>

>다른 브랜치 체크아웃하기
>### git checkout <브랜치>

> 현재 브랜치에서 새로운 브랜치 생성하고 체크아웃하기
>### git checkout -b <새로운 브랜치>

> 다른 시작 지점에서 브랜치 생성하기
>### git branch <새로운 브랜치> <브랜치를 생성할 위치>

>기존의 브랜치를 새로운 브랜치로 덮어쓰기
>### git branch -f <기존 브랜치> [<브랜치를 생성할 위치>]

> 브랜치를 옮기거나 브랜치명 변경하기
>### git checkout -m <기존 브랜치> <새로운 브랜치>

>• <새로운 브랜치>가 존재하지 않을 경우
>### git checkout -M <기존 브랜치> <새로운 브랜치>

>• 무조건 덮어쓰기


>다른 브랜치를 현재 브랜치로 합치기
>### git merge <브랜치>

> 커밋하지 않고 합치기
>### git merge - -no-commit <브랜치>

> 선택하여 합치기
>### git cherry-pick <커밋명>

> 커밋하지 않고 선택하여 합치기
>### git cherry-pick -n <커밋명>

> 브랜치의 이력을 다른 브랜치에 합치기
>### git merge - -squash <브랜치>

> 브랜치 삭제하기
>### git branch -d <삭제할 브랜치>
>• 삭제할 브랜치가 현재 브랜치에 합쳐졌을 경우에만

>### git branch -D <삭제할 브랜치>
>• 삭제할 브랜치가 현재 브랜치에 합쳐지지 않았어도


4.. Git 이력
----------

> 모든 이력 보기
>### git log

> 변경 사항을 보여주는 패치와 함께 로그 표시하기
>### git log -p

> 1개의 항목만 보이도록 로그 개수 제한하기
>### git log -1

> 20개의 항목과 패치만 보이도록 로그 제한하기
>### git log -20 -p

> 6개월 동안의 커밋 로그 보기
>### git log - -since=”6 hours”

> 이틀 전까지의 커밋 로그 보기
>### git log - -before=”2 days”

> HEAD보다 세 개 이전의 커밋 로그 보기
>### git log -1 HEAD-3
>### git log -1 HEAD^^^
>### git log -1 HEAD~1^^

> 두 지점 사이의 커밋 로그 보기
>### git log <시작 지점>…<끝 지점>
>• 시작 지점이나 끝 지점은 커밋명, 브랜치명, 혹은 태그명이 될 수 있고 조합하여 사용 가능하다.

> 각 항목의 로그 이력 한 줄씩 보기
>### git log - -pretty=oneline

> 각 항목마다 영향 받은 줄의 통계 보기
>### git log - -stat

> 커밋할 시점의 파일 상태 보기
>### git log - -name-status

> 현재 작업 트리와 인덱스의 차이점 보기
>### git diff

> 인덱스와 저장소의 차이점 보기
>### git diff - -cached

> 작업 트리와 저장소의 차이점 보기
>### git diff HEAD

> 작업 트리와 특정 위치 간의 차이점 보기
>### git diff <시작 지점>
>• 시작 지점은 커밋명 or 브랜치명 or 태그명이다.

> 저장소의 두 지점 사이의 차이점 보기
>### git diff <시작 지점> <끝 지점>

> 차이점의 통계 보기
>### git diff - -stat <시작 지점> [<끝 지점>]

> 파일의 커밋 정보 줄 단위로 보기
>### git blame <파일>

> 파일의 줄 단위의 복사, 붙여 넣기, 이동 정보 보기
>### git blame -M <파일>

> 파일의 줄 단위의 이동과 원본 파일 정보 보기
>### git blame -C -C <파일>

> 로그에서 복사와 붙여 넣은 정보 보기
>### git log -C -C -p -1 <특정 지점>


5.. 원격 저장소
----------
> 저장소 복제하기
>### git clone <저장소>

> 마지막 200개의 커밋만 포함하여 저장소 복제하기
>### git clone - -depth 200 <저장소>

> 새로운 원격 저장소 추가하기
>### git remote add <원격 저장소> <저장소 url>

> 모든 원격 브랜치 목록 보기
>### git branch -r

> 원격 브랜치에서 지역 브랜치 생성하기
>### git branch <새로운 브랜치> <원격 브랜치>

> 원격 태그에서 지역 브랜치 생성하기
>### git branch <새로운 브랜치> <원격 태그>

> origin 저장소에서 합치지 않고 지역 브랜치로 변경 사항 가져오기
>### git fetch

> 원격 저장소에서 합치지 않고 지역 브랜치로 변경 사항 가져오기
>### git fetch <원격 저장소>

> 원격 저장소에서 변경 사항을 가져와 현재 브랜치에 합치기
>### git pull <원격 저장소>

> origin 저장소에서 변경 사항을 가져와 현재 브랜치에 합치기
>### git pull

> 지역 브랜치를 원격 브랜치에 푸싱하기
>### git push <원격 저장소> <지역 브랜치>:<원격 브랜치>

> 지역 브랜치를 동일한 이름의 원격 브랜치에 푸싱하기
>### git push <원격 저장소> <지역 브랜치>

> 새로운 로컬 브랜치를 원격 저장소에 푸싱하기
>### git push <원격 저장소> <지역 브랜치>

> 원격 저장소에서 쓸모가 없어진 원격 브랜치 제거하기
>### git remote prune <원격 저장소>

> 원격 저장소를 제거하고 관련된 브랜치도 제거하기
>### git remote rm <원격 저장소>



### 위에 작성된 명령어들은 주로 사용될만한 명령어들이고 이외에도 git 의 명령어는 상당히 많다.



