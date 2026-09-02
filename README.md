# Arena: An Interactive Multi-Agent Reinforcement Learning Game

> An interactive AI game where players modify the environment and observe hiders and seekers learn and adapt through multi-agent reinforcement learning.

## 1. Introduction

Artificial Intelligence is becoming an important part of modern games. It is used to control enemies, non-playable characters, game events and many other parts of a game. In many games, the behaviour of these characters is created using fixed rules. For example, an enemy can be programmed to move towards the player when the player enters a certain area. It can also be programmed to attack when it gets close enough. These methods are useful, but the behaviour of the enemy normally remains the same throughout the game.

Our project, called **Arena**, aims to create a game where the behaviour of AI agents can change based on their experience. The game will contain two teams of AI agents called **hiders** and **seekers**. The hiders will try to avoid being found or captured by the seekers, while the seekers will try to locate and capture the hiders.

The main idea of our project is to allow the player to change the environment instead of directly controlling the AI agents. The player will be able to place objects in the arena one at a time. These objects can include walls, boxes, barriers and other objects that can affect the movement of the agents. After making changes to the arena, the player can start a simulation and watch the two teams interact with each other.

The agents will use **reinforcement learning** to improve their behaviour. During a simulation, the agents will take different actions and receive rewards or penalties based on the results of those actions. For example, a hider can receive a positive reward for staying hidden and a negative reward when it is captured. Similarly, a seeker can receive a positive reward for finding a hider.

The agents will go through many simulations. As training continues, they can improve their decisions based on what they have experienced before. This can lead to changes in the way the agents move around the arena.

For example, a hider may initially move randomly when a seeker comes close. After more training, the hider may learn that staying behind a wall gives it a better chance of remaining hidden. Later, the seeker may also learn that simply moving towards the last known position of the hider is not enough. It may start searching around the wall or checking different areas of the arena.

This creates a situation where both teams can improve because of the behaviour of the other team. If the hiders become better at hiding, the seekers have to improve their searching behaviour. If the seekers become better at finding hiders, the hiders have to find better ways to survive.

The player will be able to influence this process by changing the environment. For example, the player can add a large wall and observe how the hiders use it. In another simulation, the player can remove the wall or add several smaller obstacles and compare the results.

The game will also include a **simulation and visualization system**. The player will be able to see different generations of training and compare how the agents behave over time. Information such as the number of hiders captured, survival time, team rewards and winning team can be displayed to help the player understand what is happening.

The main purpose of Arena is therefore to create a **playable AI based product** where the player can interact with an environment and observe AI agents learning and adapting. The project combines game development with reinforcement learning and multi agent systems.

## 2. Literature Survey

### Reinforcement Learning

Reinforcement Learning is a type of machine learning where an agent learns by interacting with an environment. Instead of being given the correct answer for every situation, the agent tries different actions and receives feedback from the environment. This feedback is usually given in the form of rewards and penalties.

For example, consider an agent that needs to reach a target. If the agent moves closer to the target, it can receive a positive reward. If it moves away from the target, it can receive a small negative reward. If it reaches the target, it can receive a larger reward. After many attempts, the agent can learn which actions are more useful.

This idea can be applied to games because games naturally provide an environment, actions and possible rewards. An agent can move around the game world, interact with objects and make decisions. The game can then provide feedback based on the agent's actions.

Reinforcement Learning has been used in many game related applications. It can be used for training characters, learning game strategies and solving tasks that are difficult to handle using fixed rules. The main advantage is that the developer does not have to manually define every possible situation.

### Multi Agent Reinforcement Learning

Multi Agent Reinforcement Learning is an extension of reinforcement learning where multiple agents operate in the same environment. These agents can have different objectives. Some agents may cooperate with each other, while others may compete.

This makes the learning process more interesting because an agent has to consider the actions of other agents. The environment is not fixed from the point of view of the agent. If another agent changes its strategy, the first agent may also need to change its strategy.

One well known example of this type of learning is the **Hide and Seek environment** developed for studying multi agent reinforcement learning. In this environment, hiders and seekers are trained against each other. The hiders try to avoid being seen, while the seekers try to find them. During training, the agents can develop different behaviours based on the environment and the actions of the other team.

### Self-Play

Another important concept related to this project is **self-play**. Self-play allows agents to improve by competing against other agents. When one group becomes better, the other group has to respond to the new behaviour. This can continue over many training sessions.

This type of training can be useful in games because it can produce behaviour that is difficult to create using simple rules. Instead of telling an agent exactly how to solve a problem, the developer defines the goal and the reward system. The agent then tries to find a good way of achieving that goal.

### Unity ML-Agents

**Unity ML Agents** provides tools for creating reinforcement learning environments inside the Unity game engine. It allows developers to create agents, define their observations and actions, provide rewards and train the agents using machine learning methods.

The existing Unity ML Agents Hide and Seek project provides a useful starting point for our project because it already demonstrates a multi agent environment with hiders and seekers. It also provides an example of how agents can be trained and tested inside Unity.

However, our project will not simply reproduce the same environment. **Arena will introduce a player-controlled environment building system.** The player will be able to add objects to the arena and influence the conditions in which the agents operate.

This difference is important because it makes the project more interactive. The player will not only watch the agents after training. They will be able to experiment with the environment and see how different changes affect the behaviour of the agents.

The literature and existing work on reinforcement learning, self-play and multi agent systems therefore provide the technical foundation for Arena. Our project uses these ideas to create a game that allows the player to interact with and observe the learning process.

## 3. Comparative Analysis

There are several ways to create intelligent behaviour in games. The simplest method is to use predefined rules. More advanced methods can use pathfinding, state machines and other game AI techniques. Reinforcement learning provides another approach where the behaviour is learned from experience.

### Rule Based AI

Rule based AI is one of the most common methods used in games. In this approach, the developer directly defines the behaviour of the character.

For example, a simple seeker could use rules such as:

```text
If the hider is visible, move towards the hider.

If the hider is close, capture the hider.

If no hider is visible, move around the arena.
