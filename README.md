# RL_ML-Agent : Penguins

![Penguins_10000steps](https://github.com/Robinmncn/RL_ML-Agent/blob/master/animations/Penguins_10000steps.gif?raw=true)

## Installation

### Needed : 
- ML-Agent (v0.14.1) at : https://github.com/Unity-Technologies/ml-agents using C#

- Unity 

Once  Unity and Ml-Agent are installated, open Unity and create a new 3D project.

Now you can clone the repo inside your new project using

```jconsole
git clone https://github.com/Robinmncn/RL_ML-Agent.git
```

In this flder, go to Packages/manifest.json, open it and add a new line to add the ML-Agent Package using,

```
"com.unity.ml-agents": "[PATH-to-ML-Agent]/ml-agents-0.14.1/com.unity.ml-agents",
```

You can play the game in Unity using "ZQSD" to move (you can change that in Assets/Penguin/Scripts/PenguinAgent.cs in the Heuristic() method)

## Training

In the ML-Agent folder, run the command :

```
mlagents-learn config/trainer_config.yaml --curriculum config/curricula/penguin.yaml --run-id penguin_01 --train
```

ML-Agent will ask you to play the game. Tou will be able to see the agents learning in their new environment.

![Penguins_learning](https://github.com/Robinmncn/RL_ML-Agent/blob/master/animations/Penguins_Training.gif?raw=true)

You can also open a tensorboard to follow the agents' progress using : 

```
tensorboard --logdir=summaries
```


![Results](https://github.com/Robinmncn/RL_ML-Agent/blob/master/results_penguins.png)


## Run Inference

Once your training is over, your NN will be saved at Assets/Penguin/NNModels.

In Unity now open Assets/Penguin/prefabs and selected you NN in "Behavior Parameters", then you can run a new game to watch your agents.

## Note

Do not hesitate to contact me if you need some help
