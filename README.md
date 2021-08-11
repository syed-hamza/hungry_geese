# Hungry Geese
In this repository I am presenting my experience of participating into the kaggle competition [Hungry Geese](https://www.kaggle.com/c/hungry-geese/).

## Introduction:
I am grateful to the Kaggle team for running this competition and the community for this educative experience.
Hungry Geese involves a popular classic snake with a multiplayer twist to it. The snake travels allound a 7x11 grid attempting to grow as large as it can while avoiding collision with other geese. The longest geese surviving the 200 step game or the last surviving geese is declared the winner.

## Rules:
1) A geese is forbidden from turning in the opposite direction. (East while facing West)
2) A geese reduces its size every 40 turns. (The goose with the minimum size will starve)
3) food and geese spawn randomly on the grid.
4) Colliding with the body of another goose disqualifies the goose. (Head on collision will disqualify both geese)

## Applications:
hungry geese is a peculiar straight forward problem of reinforcement learning. Reinforcement learning has several real world applications lke logits and healthcare.
## Approach:
### input features(21 x 7 x 11)
####    1) feature 1-4 : head of geese
####    2) feature 5-8 : Tail of geese
####    3) feature 9-12: body of geese
####    4) feature 13-16: previous head position
####    5) feature 17: food
####    6) feature 18-21: possible movements

For this competition I used the public reinforcement learning library [HandyRl](https://github.com/DeNA/HandyRL) to claim the 100th position within 20 days. HandyRl is easy to use/tweak and hence vaible in a time crunch situation.

My initial aproach was the keras DQN which didn't perform well even after hours of training and tweaking which compelled me to switch algorithms.The agent [here](src/keras.ipynb) failed to perform better than the provided greedy agent even after hours of training. 

With about 15 days remaining i set up 2 sessions in microsoft azure with different model architectures and [parametres](config.yaml) to run for about 3 days. I collected about 6 best models throught games among themselves and other public agents for ensembling and final submition.

### About me
I am and 18 year old deep learning enthusiast, graduated during the pandemic. This competition gave me the title of "competition expert".

