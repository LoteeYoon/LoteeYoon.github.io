---
layout: article
title: 1. Multi Armed Bandits
tags: Reinforcement-Learning
aside:
  toc: true
key: page-aside
---

수업들은 내용을 요약 정리한 글입니다.
[David Silver lecture slide](https://www.davidsilver.uk/teaching/) 를 수업자료로 활용하였습니다.

* * *


#### Multi Armed Bandits이란?

  &nbsp;&nbsp;-> reward를 모르는 채로 slot machine을 당기는 문제와 같다

![png](/_posts/_assets/slot_machine.png)

- What makes a bandit problem?

  - 2가지 핵심 properties:

    1) reward에 대해 모르는 채로 action 선택

    2) 선택에 대해 feedback(reward)이 주어진다


- Model : Finite Armed Bandits
