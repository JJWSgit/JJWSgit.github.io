---
title:  "[멋사 AI 7기] 웹 데이터 ETC"
categories: likelion
tag: [TIL]
toc: true
author_profile: false
sidebar:
    nav: "docs"
search: true
---

:octocat:Web | DataFrame<br>
<br>

# WEB

:pushpin:참고사항<br>
네이버 증권 게시판에 글을 쓰면<br>
데이터베이스권은 네이버에 있으며 저작권은 글쓴이에게 있음<br>
<br>
get : 필요한 데이터를 Query String 에 담아 전송<br>
post : 전송할 데이터를 HTTP 메시지의 Body의 Form Data에 담아 전송<br>
get 과 post 여부는 브라우저의 네트워크 탭의 Headers > Request Method 를 통해 확인<br>
<br>

referer<br>
헤더에 담겨 있는 현재 페이지에 요청한 이전 페이지의 url 정보<br>
서버는 referer 참조함으로써 현재 표시하는 웹페이지가 어떤 웹페이지에서 요청되었는지 알 수 있음<br>
[참고 사이트](https://inpa.tistory.com/entry/WEB-%F0%9F%93%9A-HTTP-referer-%EB%9E%80)<br>

get

## 비동기 통신

XHR(XMLHttpRequest)<br>
필요한 부분만 서버에 요청하고 해당하는 내용만 받음<br>
=> 대역폭의 낭비를 줄이고 필요한 부분만 요청하는 상호작용<br>
[참고 사이트](https://velog.io/@ldaehi0205/ajax-fetch-xhr-%EB%B9%84%EB%8F%99%EA%B8%B0%ED%86%B5%EC%8B%A0-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0)<br>

# 웹 데이터 수집

## Pandas read_html

데이터를 수집할 URL을 찾고, pd.read_html(url)을 통해 table 태그의 데이터를 가져온다.<br>
한글 깨짐 방지!<br>

## BeautifulSoup

상세정보를 위한 링크정보 수집<br>
=> bs를 사용하여 수집한 html 문서에서 링크 정보를 찾는다<br>
<br>
html tag에서 사용하는 css class 지정방식과 bs에서 사용하는 방법의 차이가 있다. 확인 필요<br>
nth-child를 지원하지 않아 nth-of-type을 바꿔줘야함<br>
<br>

get_text() 는 메소드, text 는 attr 그 외에 차이가 안보임<br>


## 예외 처리

try except 구문<br>
try 구문에서 오류가 나면 except 구문으로 빠짐<br>
함수를 반복적으로 돌릴 때 중간에 오류가 나서 멈추는 경우를 방지<br>
<br>
예외 사항에서 꼭 고쳐야 하는 심각한 것에는 무엇이 있을까?<br>
보안 이슈<br>
- 크로스 사이트 스크립팅(Cross Site Scripting, XSS)<br>
'공격자'의 웹사이트에서 피해자가 친숙하다고 느끼는 웹사이트에 악성 스크립트를 주입하는 행위<br>
웹사이트 사이를 넘어서 공격한다는 의미에서 크로스 사이트 스크립팅이라는 용어가 생겨남.<br>

[참고 사이트](https://nordvpn.com/ko/blog/xss-attack/)<br> 

# DataFrame 화

T = 전치행렬 transpose()<br>
set_index(index로 만들 column)<br>
pd.concat([df1, df2,..], axis) 1 : 옆으로<br>
map, apply<br>
: 데이터프레임(특정 컬럼)에 반복문을 사용하지 않고 함수 일괄 적용<br>
<br>
<br>

<details>
<summary>:bookmark:출처</summary>

- referer<br>
https://inpa.tistory.com/entry/WEB-%F0%9F%93%9A-HTTP-referer-%EB%9E%80<br>
- XHR<br>
https://velog.io/@ldaehi0205/ajax-fetch-xhr-%EB%B9%84%EB%8F%99%EA%B8%B0%ED%86%B5%EC%8B%A0-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0<br>
- XSS<br>
https://nordvpn.com/ko/blog/xss-attack/<br>
</details>
<br>


:mortar_board:**포스팅 공지** <br><br>
작성한 포스팅은 **멋쟁이 사자처럼 AI SCHOOl**의 수업 내용입니다.<br>
{: .notice--success}
