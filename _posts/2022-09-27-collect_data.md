---
title:  "[멋사 AI 7기] 데이터 수집"
categories: likelion
tag: [TIL]
toc: true
author_profile: false
sidebar:
    nav: "docs"
search: true
---

:octocat:Web | API<br>
<br>

# 웹 데이터 수집

## 추상화된 도구

- FinanceDataReader : 한국 주식 가격, 미국주식 가격, 지수, 환율, 암호화폐 가격, 종목 리스팅 등 금융 데이터 수집 라이브러리
[FinanceData/FinanceDataReader: Financial data reader](https://github.com/FinanceData/FinanceDataReader)<br>
[FinanceDataReader 사용자 안내서 | FinanceData](https://financedata.github.io/posts/finance-data-reader-users-guide.html)<br>
- Pandas-datareader
[Pandas-datareader]https://pandas-datareader.readthedocs.io/en/latest/index.html<br>
<br>

* 참고사항<br>
selenium 추천X<br>
selenium의 원래 목적은 웹브라우저 테스트 도구<br>
속도 오래걸리고 메모리를 많이 잡아먹는 단점이 있다.<br>


## 수집 시 유의사항

- 로봇 배제 표준 : 웹 사이트에 로봇이 접근하는 것을 방지하기 위한 규약  * robots.txt : 수집해도 되는 페이지와 에이전트 정보를 알려줌<br>
로봇 배제 표준이 권고안이라도 불법으로 데이터를 수집하여 영업 혹은 저작권 침해에 해당된다면 법적 제재를 받을 수 있으니 주의!<br>
- 저작권<br>
- 무리한 네트워크 요청<br>
DDOS 공격으로 의심 받을 수 있어서 일반적으로 time.sleep() 사용<br>

## HTTP 통신과 HTML, CSS의 이해

HTML<br>
    - id    #<br>
    - class .<br>
table tag는 pandas로 불러올 수 있다.    * read_html(url) 네트워크 탭에서 URL 찾아보기<br>
<br>
CSS<br>



<br>
<br>

**포스팅 공지** <br><br>
작성한 포스팅은 **멋쟁이 사자처럼 AI SCHOOl**의 수업 내용입니다.<br>
{: .notice--success}
