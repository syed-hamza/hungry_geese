# Hungry Geese
In this repository, I am presenting my experience of participating in the Kaggle competition [Hungry Geese](https://www.kaggle.com/c/hungry-geese/).
I'm extremely happy that with a final rank of 100 I could make it into the list of Medal winners. Since it is my second medal win in Kaggle, I achieved the level of [Kaggle Expert](https://www.kaggle.com/syedhamzahussain).

## Introduction:
I am grateful to the Kaggle team for running this wonderful competition and for the helping community with this educative experience.
Hungry Geese is a popular classic snake game with a multiplayer twist to it. The snake travels around a 7x11 grid attempting to grow as large as it can while avoiding collision with other geese. The longest geese surviving the 200 step game or the last surviving geese is declared the winner.

![Game](/images/2021-08-12_01-57.png)

## Rules:
1) A geese is forbidden from turning in the opposite direction. (East while facing West)
2) A geese reduces its size every 40 turns. (The goose with the minimum size will starve)
3) food and geese spawn randomly on the grid.
4) Colliding with the body of another goose disqualifies the goose. (Head-on collision will disqualify both geese)

## Bellman Equation:
One of the most important things that I learned from this competition is the Bellman Equation. It is amazing to see how the Reinforcement Learning techniques evolved from this equation. I attended few Tutorials from Deepmind to get a quick grasp of Reinforcement Learning techniques.

![equation](/images/bellman.svg)

The [discount factor](https://stats.stackexchange.com/questions/221402/understanding-the-role-of-the-discount-factor-in-reinforcement-learning) is varied between .8 and .95.
## Approach:
Although it was an uphill task to make an impact with only one month in hand, it was achievable.

My initial approach on a policy-based agent was the [keras DQN](src/keras.ipynb) which failed to perform better than the provided greedy agent even after hours of training and tweaking. I switched to [HandyRl](https://github.com/DeNA/HandyRL) library. HandyRl is easy to use/tweak and hence viable in a time-crunch situation.

My first attempt was a rule based agent [here](src/Smarter_Greedy_Goose.ipynb).

With about 15 days remaining in hand, I set up multiple versions of DQN Deep Learning with different model architectures and [parametres](config.yaml) to run for about 7 days. Thanks to my gaming PC that is having a RTX-2070 GPU. I collected about 6 best models running through internal games among themselves and other public agents for ensembling and final submission. I uploaded a total of 63 kernels with various experiments. The ranking on the leaderboard was extremely volatile and unpredictable. It was a sign of hard battles from thousands of the agents uploaded by the participants. There was some time I was ranked 41st on the list.
### input features(21 x 7 x 11)
   1) feature 1-4 : head of geese
   2) feature 5-8 : Tail of geese
   3) feature 9-12: body of geese
   4) feature 13-16: previous head position
   5) feature 17: food
   6) feature 18-21: possible movements
### Model Architecture:
![Model](/images/architecture_model.png)


### About me
I am an 18-year-old Deep Learning enthusiast, I passed 12th Standard (CBSE) on July 2021 with an Aggregate mark of 96%. I'm interested to work in any area of Deep Learning. Earlier, I had a Silver Medal (rank 79/2097) from a Healthcare problem (OSIC Pulmonary Fibrosis Progression) in Kaggle. This win helped me to reach the title of "Kaggle Competition Expert"!
