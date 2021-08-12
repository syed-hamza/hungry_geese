# Hungry Geese
In this repository I am presenting my experience of participating into the kaggle competition [Hungry Geese](https://www.kaggle.com/c/hungry-geese/).

## Introduction:
I am grateful to the Kaggle team for running this competition and the community for this educative experience.
Hungry Geese involves a popular classic snake with a multiplayer twist to it. The snake travels allound a 7x11 grid attempting to grow as large as it can while avoiding collision with other geese. The longest geese surviving the 200 step game or the last surviving geese is declared the winner.

![Game](/images/2021-08-12_01-57.png)


## Rules:
1) A geese is forbidden from turning in the opposite direction. (East while facing West)
2) A geese reduces its size every 40 turns. (The goose with the minimum size will starve)
3) food and geese spawn randomly on the grid.
4) Colliding with the body of another goose disqualifies the goose. (Head on collision will disqualify both geese)

## Bellman Equation:
![equation](/images/bellman.svg)

The discount factor is varied between .8 and .95.
## Approach:
I participated to Hungry Geese with one month left for this 6-month long competition.Although it was an uphill task to make an impact with only one month in hand, it was acheivable. Initially, I started with Keras library of Reinforcement learning but I switched to [HandyRl](https://github.com/DeNA/HandyRL) library. HandyRl is easy to use/tweak and hence vaible in a time crunch situation.

My initial aproach was the [keras DQN](src/keras.ipynb) which didn't perform well even after hours of training and tweaking which compelled me to switch algorithms. The agent failed to perform better than the provided greedy agent even after hours of training. 

With about 15 days remaining in hand, I set up multiple versions of DQN Deep Learning with different model architectures and [parametres](config.yaml) to run for about 7 days. Thanks to my gaming PC that is having a RTX-2070 GPU. I collected about 6 best models throught games among themselves and other public agents for ensembling and final submition.
### input features(21 x 7 x 11)
   1) feature 1-4 : head of geese
   2) feature 5-8 : Tail of geese
   3) feature 9-12: body of geese
   4) feature 13-16: previous head position
   5) feature 17: food
   6) feature 18-21: possible movements
### Model Architecture:
![Model](/images/architecture.png)



### About me
I am and 18 year old Deep Learning enthusiast, I passed 12th Standard (CBSE) on July, 2021 with Agregate 96%. I'm extremely happy to figure in a list of Medal winners in Hungry Geese. Earlier, I had a Silver Medal (rank 79/2097) from a Healthcare problem (OSIC Pulmonary Fibrosis Progression) in Kaggle. This win helped me to reach the title of "Kaggle Competition Expert"!

