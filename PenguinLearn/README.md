# ml-penguins-upgrade

## Intro

Unity partnered with Immersive Limit LLC to release a tutorial for ML-Agents called Penguins that gave users an introduction to ML-Agents in Unity.  Just recently, Unity released an official package of ML-Agents that has a ton of new and updated features.  The version of ml-agents that is used in the tutorial is a little dated and I wanted to provide updated code for users who are interested in using the new package.

https://learn.unity.com/project/ml-agents-penguins

## Setup

1. Download and install Unity 2019.3.x from the Unity Hub
2. Pull the newest ML-Agents release from the Github and install the ML-Agents preview package in Unity.
https://github.com/Unity-Technologies/ml-agents/releases

3. Download and install Anaconda from the link below:
https://www.anaconda.com/distribution/
Follow the same set-up process to get ml-agents set-up in Anaconda.

4. Download this project to your local machine.

5. Open the project in Unity

6. Open the Sample Scene in Penguin/Scenes

7. Follow the last tutorial to add the content to the trainer_config.yaml and penguin.yaml files.  The content to be added can be found in the Penguin folder (add the trainer_config block to the end)

8. Connect the inference engine to Unity to train the penguins and generate a NN model.

```bash
mlagents-learn config/trainer_config.yaml --curriculum config/curricula/penguin --run-id penguin_01 --train
```

9. Add your NN model to the Model field under the Behavior Parameters component on the Penguin.
10. Hit play to have your penguin go through and collect the fish based on the model that was developed.
