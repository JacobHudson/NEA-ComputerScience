# AI locomotion

*Teaching a bipedal AI to walk using inverse kinimatics along a unpredictable, procedural terrain.*

By Jacob Hudson

[TODO List](https://trello.com/b/40AqKOCt/ai-locomotion)

## Technologies
### Terrain Generation?
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

[Jacobian]()

[CCD]()

## Papers and Research
[Proximal Policy Optimization Paper, OpenAI](https://arxiv.org/pdf/1707.06347.pdf)

[Reinforcement Learning Algorithms Git Repo, OpenAI](https://github.com/openai/baselines)

[Teaching AI to Walk Video, Code Bullet](https://youtu.be/9amJuvb3grU?list=TLPQMDgwNTIwMjOCUIFdAmslIg)

[Mathematics for Inverse Kinematics Paper, CMU, Ming Yao](https://www.cs.cmu.edu/~15464-s13/lectures/lecture6/IK.pdf)

[Oh My God, I Inverted Kine! Jeff Lander](http://www.darwin3d.com/gamedev/articles/col0998.pdf)

[Making Kine More Flexible, Jeff Lander](https://www.cs.cmu.edu/~15464-s13/lectures/lecture6/jlander_gamedev_nov98.pdf)

https://iclr-blog-track.github.io/2022/03/25/ppo-implementation-details/

https://www.geeksforgeeks.org/a-brief-introduction-to-proximal-policy-optimization/

https://arxiv.org/pdf/1707.06347.pdf

https://openai.com/research/openai-baselines-ppo

## Notes from similar Projects
- The T pose is just a bit back heavy, so they naturally fall back and continue there movement in that direction. Start with weight in forwards direction.
- Friction is not quite correct making it not actually use their legs to push forward but their lean over weight to pull them.
- Every bone is the same weight and every joint the same strength which causes strange priorities. 
- Movement of toes plays an important role when walking and running, so adding another joint behind the toes might help a lot for AI to learn walking. 
- Killing them only when their head touch the ground and giving serious penalty points for touching their body parts (may differ for front and back also) other than bottom of the feet, also giving less penalty points for hands may force them to learn getting up when they fall. 
- Encouraging the chest to point at the target would help immensely.
