---
title:  "[멋사 AI 7기] 랜덤포레스트"
categories: likelion
tag: [TIL]
toc: true
author_profile: false
sidebar:
    nav: "docs"
search: true
---

:octocat: modeling<br>
<br>

# DecisionTree

**장점**<br>
baseline model로 좋다<br>
부스팅 모델의 기반이고 빠르며, 피처 중요도 보기 좋음<br>
**단점**<br>
랜덤성에 따라 결과 또는 성능의 변동 폭이 크다<br>
계층적 접근 방식이기 때문에 중간에 에러 발생하면 다음 단계로 에러가 계속 전파<br>
노이즈에 민감하다 ~ 과적합 가능성, 일반화하여 사용하기 어렵다<br>
<br>

# 랜덤포레스트

bagging : bootstrap + aggregating<br>
조금씩 다른 훈련 데이터에 대해 훈련된 기초 분류기(base learner)들을 결합(aggregating)시키는 방법이다.<br>
비상관화된 여러 트리들의 집계는 노이즈에 대해 강인<br>
랜덤화를 통해 좋은 일반화 성능<br>
<br>

## 주요 파라미터

n_estimators : 트리수<br>
n_jobs=k : Parallelization, -1 일때는 사용가능한 모든 코어 사용)<br>

트리가 많아서 시각화 하기가 힘들다<br>
[시각화 방법](https://github.com/andosa/treeinterpreter)<br>
<br>

**검증**
- Hold-out Validation<br>
빠르게 평가가 가능<br>
- Cross Validation
**장점**<br>
모든 데이터 셋을 평가에 활용할 수 있고, 평가에 사용되는 데이터셋의 편향을 막을 수 있다<br>
=> 데이터 부족으로 인한 underfitting 방지<br>
=> 평가 결과에 따라 좀 더 일반화된 모델을 만들 수 있다<br>
~ 정확도를 향상시킬 수 있다.<br>
<br>

**단점**
모델 훈련 및 평가 시간이 오래 걸린다<br>
<br>

**평가**
- MAE(Mean Absolute Error)<br>
- R^2 결정계수<br>
<br>

# 오늘의 이모저모

기타사항<br>
wandb : 튜닝을 하고 기록을 해주는 라이브러리<br>

:bulb:[올바른 이력서 쓰기](https://speakerdeck.com/weirdx/99con-junieo-gaebaljayi-iryeogseo-sseugi-idongug)<br>
날짜순 내림차순<br>
zip x<br>
본인 소개엔 기여점 쓰기. 기술 / 협업 / 소통<br>
기술스택 - 할 수 있는 것(주력기술)들 모호하지않게 한줄정리<br>
무관한 경력이라도 쓰는 것 추천. 조직생활 경험이나 성실성 등을 보여줄 수 있다. 어떻게 풀어쓰느냐!<br>
[이력서](https://jojoldu.github.io/)<br>
<br>
<br>

<details>
<summary>:bookmark:출처</summary>

- DecisionTree<br>
https://scikit-learn.org/stable/index.html<br>
https://scikit-learn.org/stable/tutorial/machine_learning_map/index.html<br>
- RandomForest<br>
asdasdsadsad<br>
https://github.com/andosa/treeinterpreter<br>
- 99CON : 주니어 개발자의 이력서 쓰기 - 이동욱<br>
https://speakerdeck.com/weirdx/99con-junieo-gaebaljayi-iryeogseo-sseugi-idongug<br>
https://jojoldu.github.io/<br>
</details>
<br>


:mortar_board:**포스팅 공지** <br><br>
작성한 포스팅은 **멋쟁이 사자처럼 AI SCHOOl**의 수업 내용입니다.<br>
{: .notice--success}