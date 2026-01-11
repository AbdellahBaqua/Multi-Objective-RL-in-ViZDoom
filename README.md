\# Multi-Objective Reinforcement Learning in ViZDoom 



\### Dynamic Preference Adaptation via Conditioned Proximal Policy Optimization (c-PPO)





\*\*Zero-Shot Adaptation in Visuomotor Control.\*\*

This project implements a single Reinforcement Learning agent capable of switching behavior instantly between \*\*Aggression\*\*, \*\*Ammo Conservation\*\*, and \*\*Survival\*\* without retraining.



---





\## Abstract



In the standard \*\*ViZDoom: Defend the Center\*\* scenario, a "Turret's Dilemma" exists where maximizing kills often leads to ammo waste and early death. Standard RL optimizes a single scalar reward, failing to capture the trade-offs between conflicting objectives.



We propose a \*\*Conditioned PPO (c-PPO)\*\* framework. By treating the environment as a \*\*Multi-Objective Markov Decision Process (MOMDP)\*\*, the agent receives both the visual input (screen) and a user-defined \*\*Preference Vector ($\\omega$)\*\*. This allows the agent to dynamically prioritize:

1\.  \*\*Combat Effectiveness\*\* ($r\_{kill}$)

2\.  \*\*Resource Efficiency\*\* ($r\_{ammo}$)

3\.  \*\*Survivability\*\* ($r\_{pain}$)



---



\##  Project Structure



Here is the description of the files included in this repository:



```text

/

│

├── multiobj.ipynb         #  Multiobjective test

├── initial.ipynb          #  Setup \&  baseline test

│

├── model\_Berserker.zip    #  Trained Model (Aggressive weights)

├── model\_Sentinel.zip     #  Trained Model (Survival weights)

├── model\_Tactician.zip    #  Trained Model (Balanced weights)

│

├── gameplay\_hdBersk.gif   #  HD Recording: Berserker profile

├── gameplay\_hdSent.gif    #  HD Recording: Sentinel profile

├── gameplay\_hdTact.gif    #  HD Recording: Tactician profile

│

├── Berserker/             #  Tensorboard Logs for Berserker training

├── Sentinel/              #  Tensorboard Logs for Sentinel training

└── Tactician/             #  Tensorboard Logs for Tactician training



