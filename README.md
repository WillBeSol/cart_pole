# OpenAi CartPole
*****************


.. contents:: **Contents of this document**
   :depth: 2


Installation
------------

.. code:: shell

    pip install requirement.txt
    or
    pip install tensorflow==1.4.1 gym==0.7.0 matplotlib==2.1.2

..

Run
===

.. code:: shell

    cd cart_pole
    python dqn_agent.py


Description
===========

 cart_pole 예제의 goal은 최대한 오랫동안 막대기를 세우고 있는 것입니다.

 이 system은 track과 cart와 joint, pole로 이루어져 있습니다.
 cart는 track위에서 마찰없이 움직이며 cart와 pole은 자유로운 joint로 연결되어있어서 pole이 joint를 중심으로 자유롭게 회전할 수 있습니다.

 이 system에는 중력이 작용하고 있어서 가만히 놔두면 pole은 밑으로 떨어지게 됩니다.
 따라서 agent는 cart는 왼쪽 아니면 오른쪽으로 움직여서 pole을 세워놓아야합니다.

 reward는 pole이 세워져있는 시간인데 애초에 이 episode는 pole이 수직에서 15도 떨어지거나 가운데로부터 2.4units 만큼 떨어진다면 끝나게 되어있습니다.
 따라서 episode가 유지되는 시간자체가 reward가 됩니다.

 이 예제에서는 Q-learning(예제없이 학습하는 방법)과 CNN(Convolution Neural Network) 알고리즘을 사용하였습니다.

 save_graph directory 안의 CartPole_DQN.png 파일은 매 episode가 진행됨에 따라 지금까지 진행해온 episodes 중에 마지막 100개의 평균 reward를 dot형태로 보여줍니다.
 CartPole_DQN.png를 보면 episode가 진행됨에 따라 점점 평균 reward 값이 커짐을 볼수 있습니다. 이는 pole가 세워져있는 시간이 길어짐을 의미하고 학습에 의해 이 시간이 늘어났음을 의미합니다.


