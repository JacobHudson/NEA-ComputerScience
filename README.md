# AI locomotion

*Teaching a bipedal AI to walk using inverse kinimatics along a unpredictable, procedural terrain.*

By Jacob Hudson

## Technologies
### Terrain Generation
#### Idea
Create a small, low-poly area of land suitable for exploration by a humanoid character.
#### Algorithms
[Marching cubes](https://en.wikipedia.org/wiki/Marching_cubes)

### Artificial Intelligence
#### Idea
Generational learning using a points system to determine its level of success. The ai will have vision based on raycasts allowing it to be aware of its surroundings.
#### Algorithms
[PPO](https://openai.com/research/openai-baselines-ppo)

### Inverse Kinematics
#### Idea
New foot point is determined by the ai, then with the use of IK the rest of the body can be balanced and moved to its new position.
#### Algorithms
[Unity built in IK](https://docs.unity3d.com/Manual/InverseKinematics.html#:~:text=This%20can%20be%20useful%20when%20you%20want%20a,any%20humanoid%20character%20with%20a%20correctly%20configured%20Avatar.)

## Papers and Research
[Proximal Policy Optimization Paper, OpenAI](https://arxiv.org/pdf/1707.06347.pdf)

[Reinforcement Learning Algorithms Git Repo, OpenAI](https://github.com/openai/baselines)

[Teaching AI to Walk Video, Code Bullet](https://youtu.be/9amJuvb3grU?list=TLPQMDgwNTIwMjOCUIFdAmslIg)
