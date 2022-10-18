---
title:  "[멋사 AI 7기] Git과 Streamlit"
categories: likelion
tag: [TIL]
toc: true
author_profile: false
sidebar:
    nav: "docs"
search: true
---

:octocat: git/github & streamlit<br>
<br>

# Git 과 GitHub

- git : 분산(여러 사용자들의 작업/수정) 버전 관리 시스템<br>
컴퓨터 파일의 변경사항을 추적하는 시스템<br>
여러 명의 사용자들 간에 해당 파일들의 작업을 조율하기 위한 스냅샷 스트림 기반의 분산 버전 관리 시스템<br>
git은 빠른 수행 속도에 중점을 두고 있는 것이 특징이며 데이터 무결성, 분산, 비선형 워크플로를 지원<br>
<br>

- github : 소스코드 관리 + 저장 + 소셜코딩<br>
분산 버전 관리 툴인 깃 저장소 호스팅을 지원하는 웹 서비스이다.<br>
<br>

## [commit](https://backlog.com/git-tutorial/kr/intro/intro1_3.html) / [git commit](https://steady-coding.tistory.com/m/277)

버전관리의 일환<br>
버전은 의미 있는 변화를 뜻하며, 작업이 완결된 상태<br>
이렇게 의미 있는 변화에 대해 기록하는 것이 바로 commit<br>
변경을 기록하는 커밋, 파일 및 폴더의 추가/변경 사항을 저장소에 기록<br>
<br>

## repository 만들기

- gitignore : 파일을 git의 추적에서 제외 - 올릴 필요없는 캐시/로그 등의 파일 저장하지마라<br>
Project에 원하지 않는 Backup File이나 Log File , 혹은 컴파일 된 파일들을 Git에서 제외시킬수 있는 설정 File이다.<br>
항상 최상위 Directory에 존재해야함<br>
규칙을 작성하여 특정 확장자를 제외할 수 있다.<br>
- LICENSE [참고](https://wooono.tistory.com/m/379)<br>
- README.md<br>
[깃헙 마크다운 문서](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)<br>
<br>

[imgur](https://imgur.com/) : 이미지 업로드 후 링크 사용할 때 괜찮은 사이트<br>
<br>

pip freeze > requirements.txt : 설치된 패키지를 목록으로 만들기<br>
requirements.txt<br>
필요한 모듈/라이브러리 알려주는 약속<br>
배포 할 때 사용하면 서버에 필요한 패키지를 설치해 줌<br>
pandas=1.5 처럼 버전을 지정해서 목록화 할 수 있다.<br>
<br>

# streamlit [시작하기](https://docs.streamlit.io/library/get-started)

st.markdown<br>
st.sidebar<br>
- markdown<br>
- header<br>
- selectbox<br>
- multiselect<br>
<br>
st.dataframe<br>

Chart element<br>
- line_chart<br>
- bar_chart<br>
- pyplot<br>
<br>

@st.cache : 캐시 적용하기<br>
첫 로드 후 이후 기존 로드한 데이터를 사용하여 부담을 줄여준다.<br>
캐시를 적용하지 않으면 데이터를 매번 가져와야 해서 속도가 떨어짐<br>
<br>

:pushpin: plotly express 그래프 호환 잘되는편<br>
<br>

# 오늘의 이모저모

데이터센터나 클라우드 서버를 사용하는 이유?<br>
안전성, 확장성, 이원화 <br>
전력사용 및 대용량, 발열 때문<br>
<br>
:bulb: 서버 관리에 대한 불편함<br>
24시간 계속 가동되어야하는데 서버가 버티지 못해서 주기적으로 교체 해야함<br>
<br>
이모지 단축키: window + .<br>
<br>
<br>

<details>
<summary>:bookmark:출처</summary>

- Commit<br>
https://backlog.com/git-tutorial/kr/intro/intro1_3.html<br>
https://steady-coding.tistory.com/m/277<br>
- LICENSE<br>
https://pandas.pydata.org/docs/reference/api/pandas.to_numeric.html<br>
- GitHub basic writing and formatting syntax<br>
https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax<br>
- imgur<br>
https://imgur.com/<br>
- Streamlit<br>
https://docs.streamlit.io/library/get-started<br>
</details>
<br>


:mortar_board:**포스팅 공지** <br><br>
작성한 포스팅은 **멋쟁이 사자처럼 AI SCHOOl**의 수업 내용입니다.<br>
{: .notice--success}