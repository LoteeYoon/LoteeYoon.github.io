---
layout: article
title: Deep Reinforcement Learning
tags: Deepmind=Articles
aside:
  toc: true
key: page-aside
---

#### 매일 Deepmind blog post 한 편 읽기

&nbsp;&nbsp;&nbsp;&nbsp;Deepmind > Blog > [Deep Reinforcement Learning](https://deepmind.com/blog/article/deep-reinforcement-learning){: target="_blank"}

&nbsp;&nbsp;&nbsp;&nbsp;authors : David Silver
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;Date : 17 Jun 2016

---

>Humans excel at solving a wide variety of challenging problems, from low-level motor control through to high-level cognitive tasks. Our goal at DeepMind is to create artificial agents that can achieve a similar level of performance and generality. Like a human, our agents learn for themselves to achieve successful strategies that lead to the greatest long-term rewards. This paradigm of learning by trial-and-error, solely from rewards or punishments, is known as reinforcement learning (RL). Also like a human, our agents construct and learn their own knowledge directly from raw inputs, such as vision, without any hand-engineered features or domain heuristics. This is achieved by deep learning of neural networks. At DeepMind we have pioneered the combination of these approaches - deep reinforcement learning - to create the first artificial agents to achieve human-level performance across many challenging domains.

---

인간은 저차원의 motor control에서부터 고차원의 인지 작업에 이르기까지 다양한 문제를 해결하는 데 탁월하며, Deepmind의 목표는 인간과 비슷한 수준의 능력을 달성할 수 있는 artificial agents를 만드는 것이라고 합니다.
<br/>

Deepmind의 agent는 인간처럼 Long-term rewards를 가장 크게 이끌어내는 전략을 스스로 학습하고, 이러한 시행착오에 의한 학습 paradigm을 RL이라고 합니다. 또한, agent는 어떠한 hand-engineered features나 domain heuristics 없이 단순히 vision과 같은 raw inputs로부터 학습이 가능한데, 이는 neural networks에 의해 가능해졌습니다.
<br/>

Deepmind는 여러 분야에서 human-level의 성능을 달성할 수 있는 agents를 만들기 위해 위의 approache들의 조합을 여러 방식으로 개척했다고 합니다.

---

>Two years ago we introduced the first widely successful algorithm for deep reinforcement learning. The key idea was to use deep neural networks to represent the Q-network, and to train this Q-network to predict total reward.

---

2년 전, Deepmind는 deep reinforcement learning에서 처음으로 성공적인 알고리즘을 소개했습니다.
핵심 아이디어는 Q-network를 deep neural network로 나타내고, total reward를 예측하기 위해 이 신경망을 학습시키는 것입니다.

---

>Previous attempts to combine RL with neural networks had largely failed due to unstable learning. To address these instabilities, our Deep Q-Networks (DQN) algorithm stores all of the agent's experiences and then randomly samples and replays these experiences to provide diverse and decorrelated training data.

---

neural network와 RL을 결합하려는 이전의 시도에서는 불안정한 학습때문에 실패했었는데, 이러한 문제를 해결하기 위해 DQN 알고리즘은 agent의 모든 experiences를 저장해놓고 random sampling을 통해 decorrelated training data를 만들어 학습에 이용했습니다.
<br/>

Nature에 발표한 논문에서 50개의 서로 다른 Atari 게임에 DQN agent를 적용했더니 거의 절반의 게임에서 인간 수준의 성능을 달성했다고 합니다. 이는 이전의 어떤 방식보다 월등히 높은 수치라고 하네요.

![Image](https://raw.github.com/LoteeYoon/LoteeYoon.github.io/master/_posts/_assets/Atari2600.jpg)


---

>We have subsequently improved the DQN algorithm in many ways: further stabilising the learning dynamics; prioritising the replayed experiences; normalising, aggregating and re-scaling the outputs. Combining several of these improvements together led to a 300% improvement in mean score across Atari games; human-level performance has now been achieved in almost all of the Atari games.

---

차후 dynamics 안정화, experiences 우선순위화 그리고 output을 normalising, aggregating, re-scaling 하는 방식으로 DQN을 발전시켰더니 Atari 게임에서 평균 점수가 300%가 넘게 향상되었다고 합니다. 이젠 거의 모든 아타리 게임에서 인간 수준의 성능이 달성된 것입니다.

---

>We recently introduced an even more practical and effective method based on asynchronous RL. This approach exploits the multithreading capabilities of standard CPUs. The idea is to execute many instances of our agent in parallel, but using a shared model. This provides a viable alternative to experience replay, since parallelisation also diversifies and decorrelates the data.

---

Deepmind는 Deep Q-network 이외에도 Asynchronous RL을 기반으로 한 훨씬 더 실용적이고 효과적인 방법을 도입했습니다. 아이디어는 agent가 많은 instance를 병렬로 실행하지만 모델을 공유하는 것입니다. 이는 병렬화가 데이터를 diversify 하고 decorrelate 하기 때문에 experience replay를 대체할 수 있다고 합니다.

---

>Our asynchronous actor-critic algorithm, A3C, combines a deep Q-network with a deep policy network for selecting actions. It achieves state-of-the-art results, using a fraction of the training time of DQN and a fraction of the resource consumption of Gorila.

---

Asynchronous actor-critic 알고리즘인 A3C는 action을 선택하기 위해 deep policy network를 deep Q-network와 결합합니다. 이는 DQN의 trainig time 일부와 Gorila의 자원 일부를 사용하여 SOTA를 달성했다고 합니다.
