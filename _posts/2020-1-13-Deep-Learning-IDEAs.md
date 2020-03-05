---
layout: post
title: Deep Learning IDEAs
subtitle: ideas for test, paper
categories: intelligence
tags: deeplearning
comments: true
---

1. assumeing stereo images, overlapping small regions. 
From the depth information which can be extracted from the overlapping region, generating the whole information of depth of entire images.

2. Weakly supervised - dilated + transpoed convolutional feature map.

3. 잡식동물의 딜레마 (Omnivore's Dilemma)
잡식동물은 뭐든 먹기 때문에 먹던 것만 먹을 것이냐() 새로운 것을 찾을것이냐의 고민이 항상 있다. 진보적인 개체들은 도전을 해서 성공을 할 것이지만, 극단적으로 죽을 수도 있다. 보수적인 개체들은 살아남들 확률이 높지만, 새로운 발견이나 진일보를 할 가능성이 낮다. 사회는 두 가지 방향이 섞여있다는 점에서 참고하여 게임을 고안해보자. 여기서 잘못된 방향은 없다. 너무 진보적이면 지식이 쌓인다는 점에서 좋을지도 모르지만, 개체 수는 줄어든다. 또한 각 개체에게 죽음은 아주 큰 패널티이다. 그러나 새로운 발전을 하면 개체수가 나중에 커질 수 있는 가능성이 있다. (먹을 종류가 늘어나서)  너무 보수적이면 개체 수는 유지할 수 있지만, 좀 더 늘어날 수 있는 가능성을 포기하는 결과가 된다.
* 게임을 어떻게 구성하는 것이 좋을까?
기본적으로 한 사회가 모두 진보적이거나 모두 보수적이진 않다. 각각 사회는 비율은 다르지만 섞여져 있다. 보수적인 사람들은 기존의 시스템을 유지하며 사회를 돌리며, 진보적인 사람들은 시도하며 기존의 시스템을 발전시킨다. 
이는 강화학습의 탐색(exploration), 개발(exploitation)의 관계와 비슷하다. (진보-탐색, 보수-개발) 
사실 강화학습에 탐색vs개발 문제를 다룰 때 이 사회적 구조를 차용해서 사용하면 어떨까 해서 가져온 것이다. 
문제를 직접 적용하기 위해서는 1) 어떤 식으로 기존 문제를 개발시킬껀가?(보수) 2) 어떤 식으로 새로운 것을 탐구할 것인가?(진보) 3) 탐구에서 배운것을 어떻게 기존 방법에 정의할 것인가? 를 정의 해야 한다. 

4. SLAM...
4.1) 카메라의 intrinsic parameter K를 모델링(리니어+물리모델) 하는 대신 딥러닝으로? + 여러 다른 카메라들에서 쓰기 위해서 generalization하고 meta-learning을 통해서 few-sample들로 금방 찾을 수 있게?
    - intrinsic/extrinsic 파라미터 구하기? - 후자의 경우 카메라끼리나 센서와의 align 찾아내기?
4.2) 스테레오/모노 시퀀셜 데이터로 맵만들기? 어떤 방법으로 표현? 표현 방법이 정해져야 최적의 표현 방법을 찾는다?
    - 이미지들에서 매핑? (photo tourism), 카메라 로컬라이제이션?, 모델 만든 다음 임의 위치/자세에서 제너레이션? 모델을 표현하는 방법? 
    - photo tourism: http://phototour.cs.washington.edu/
