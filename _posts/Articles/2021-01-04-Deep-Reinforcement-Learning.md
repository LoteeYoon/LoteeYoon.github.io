---
layout: article
title: Deep Reinforcement Learning
tags: Articles
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

---

![image](./_posts/_assets/Atari2600.jpg)
