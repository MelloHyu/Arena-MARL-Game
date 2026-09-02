Arena: An Interactive Multi-Agent Reinforcement Learning Game

1. Introduction

Artificial Intelligence is becoming an important part of modern games.
It is used to control enemies, non-playable characters, game events and
many other parts of a game. In many games, the behaviour of these
characters is created using fixed rules. For example, an enemy can be
programmed to move towards the player when the player enters a certain
area. It can also be programmed to attack when it gets close enough.
These methods are useful, but the behaviour of the enemy normally
remains the same throughout the game.

Our project, called Arena, aims to create a game where the behaviour of
AI agents can change based on their experience. The game will contain
two teams of AI agents called hiders and seekers. The hiders will try to
avoid being found or captured by the seekers, while the seekers will try
to locate and capture the hiders.

The main idea of our project is to allow the player to change the
environment instead of directly controlling the AI agents. The player
will be able to place objects in the arena one at a time. These objects
can include walls, boxes, barriers and other objects that can affect the
movement of the agents. After making changes to the arena, the player
can start a simulation and watch the two teams interact with each other.

The agents will use reinforcement learning to improve their behaviour.
During a simulation, the agents will take different actions and receive
rewards or penalties based on the results of those actions. For example,
a hider can receive a positive reward for staying hidden and a negative
reward when it is captured. Similarly, a seeker can receive a positive
reward for finding a hider.

The agents will go through many simulations. As training continues, they
can improve their decisions based on what they have experienced before.
This can lead to changes in the way the agents move around the arena.

For example, a hider may initially move randomly when a seeker comes
close. After more training, the hider may learn that staying behind a
wall gives it a better chance of remaining hidden. Later, the seeker may
also learn that simply moving towards the last known position of the
hider is not enough. It may start searching around the wall or checking
different areas of the arena.

This creates a situation where both teams can improve because of the
behaviour of the other team. If the hiders become better at hiding, the
seekers have to improve their searching behaviour. If the seekers become
better at finding hiders, the hiders have to find better ways to
survive.

The player will be able to influence this process by changing the
environment. For example, the player can add a large wall and observe
how the hiders use it. In another simulation, the player can remove the
wall or add several smaller obstacles and compare the results.

The game will also include a simulation and visualization system. The
player will be able to see different generations of training and compare
how the agents behave over time. Information such as the number of
hiders captured, survival time, team rewards and winning team can be
displayed to help the player understand what is happening.

The main purpose of Arena is therefore to create a playable AI based
product where the player can interact with an environment and observe AI
agents learning and adapting. The project combines game development with
reinforcement learning and multi agent systems.

2. Literature Survey

Reinforcement Learning is a type of machine learning where an agent
learns by interacting with an environment. Instead of being given the
correct answer for every situation, the agent tries different actions
and receives feedback from the environment. This feedback is usually
given in the form of rewards and penalties.

For example, consider an agent that needs to reach a target. If the
agent moves closer to the target, it can receive a positive reward. If
it moves away from the target, it can receive a small negative reward.
If it reaches the target, it can receive a larger reward. After many
attempts, the agent can learn which actions are more useful.

This idea can be applied to games because games naturally provide an
environment, actions and possible rewards. An agent can move around the
game world, interact with objects and make decisions. The game can then
provide feedback based on the agent's actions.

Reinforcement Learning has been used in many game related applications.
It can be used for training characters, learning game strategies and
solving tasks that are difficult to handle using fixed rules. The main
advantage is that the developer does not have to manually define every
possible situation.

Multi Agent Reinforcement Learning is an extension of reinforcement
learning where multiple agents operate in the same environment. These
agents can have different objectives. Some agents may cooperate with
each other, while others may compete.

This makes the learning process more interesting because an agent has to
consider the actions of other agents. The environment is not fixed from
the point of view of the agent. If another agent changes its strategy,
the first agent may also need to change its strategy.

One well known example of this type of learning is the Hide and Seek
environment developed for studying multi agent reinforcement learning.
In this environment, hiders and seekers are trained against each other.
The hiders try to avoid being seen, while the seekers try to find them.
During training, the agents can develop different behaviours based on
the environment and the actions of the other team.

Another important concept related to this project is self-play.
Self-play allows agents to improve by competing against other agents.
When one group becomes better, the other group has to respond to the new
behaviour. This can continue over many training sessions.

This type of training can be useful in games because it can produce
behaviour that is difficult to create using simple rules. Instead of
telling an agent exactly how to solve a problem, the developer defines
the goal and the reward system. The agent then tries to find a good way
of achieving that goal.

Unity ML Agents provides tools for creating reinforcement learning
environments inside the Unity game engine. It allows developers to
create agents, define their observations and actions, provide rewards
and train the agents using machine learning methods.

The existing Unity ML Agents Hide and Seek project provides a useful
starting point for our project because it already demonstrates a multi
agent environment with hiders and seekers. It also provides an example
of how agents can be trained and tested inside Unity.

However, our project will not simply reproduce the same environment.
Arena will introduce a player-controlled environment building system.
The player will be able to add objects to the arena and influence the
conditions in which the agents operate.

This difference is important because it makes the project more
interactive. The player will not only watch the agents after training.
They will be able to experiment with the environment and see how
different changes affect the behaviour of the agents.

The literature and existing work on reinforcement learning, self-play
and multi agent systems therefore provide the technical foundation for
Arena. Our project uses these ideas to create a game that allows the
player to interact with and observe the learning process.

3. Comparative Analysis

There are several ways to create intelligent behaviour in games. The
simplest method is to use predefined rules. More advanced methods can
use pathfinding, state machines and other game AI techniques.
Reinforcement learning provides another approach where the behaviour is
learned from experience.

Rule Based AI

Rule based AI is one of the most common methods used in games. In this
approach, the developer directly defines the behaviour of the character.

For example, a simple seeker could use rules such as:

If the hider is visible, move towards the hider.

If the hider is close, capture the hider.

If no hider is visible, move around the arena.

This approach is easy to understand and implement. It also gives the
developer a lot of control over the behaviour. However, the agent cannot
normally create a new strategy unless the developer adds another rule.

This can become a problem when the environment becomes more complicated.
If the player adds new objects to the arena, the developer may need to
write additional rules to handle those objects.

Traditional Game AI

Traditional game AI can use methods such as state machines and
pathfinding. A character can have different states such as searching,
chasing, attacking and returning to a certain location.

Pathfinding can also help characters find a route around obstacles.
These methods can produce good results and are still widely used in
games.

However, these systems usually depend on behaviours created by the
developer. The character can choose between predefined actions, but it
does not learn from previous games in the same way as a reinforcement
learning agent.

Single Agent Reinforcement Learning

Single agent reinforcement learning allows an agent to learn through
interaction with its environment. The agent can receive rewards for
achieving its objective and penalties for making poor decisions.

This approach can create adaptive behaviour. However, it is designed
around a single learning agent or a situation where other characters are
not also learning.

Our project involves multiple agents that can affect each other. Because
of this, a multi agent approach is more suitable.

Multi Agent Reinforcement Learning

Multi Agent Reinforcement Learning allows multiple agents to learn in
the same environment. The agents can have different objectives and can
compete or cooperate.

In Arena, the hiders and seekers have opposite objectives. A successful
strategy for one team can make the other team's task more difficult.

For example, if the hiders learn to use walls effectively, the seekers
may have to change how they search. If the seekers learn to search
behind walls, the hiders may need to find other hiding locations.

This creates a changing environment where the strategies of the agents
can affect each other.

Arena

Arena combines multi agent reinforcement learning with player
interaction.

The player will be able to place objects in the arena and then start a
simulation. The agents will operate in the new environment and continue
their training.

The product can also show the progress of the agents over different
generations. This allows the player to compare the early behaviour of
the agents with their behaviour after more training.

Feature        Rule Based AI  Single Agent   Multi Agent RL Arena
RL

Learning from  No             Yes            Yes            Yes
experience

Multiple AI    Possible       Limited        Yes            Yes
agents

Competition    Limited        Limited        Yes            Yes
between agents

Environment    Limited        Yes            Yes            Yes
changes

Player changes No             No             Usually No     Yes
environment

Strategy can   No             Yes            Yes            Yes
change through
training

Training       No             Yes            Yes            Yes
generations

Learning can   Limited        Possible       Possible       Yes
be shown to
player

The main difference between Arena and a normal reinforcement learning
demonstration is the role of the player. The player is given control
over the environment instead of directly controlling the agents.

This gives the player a reason to experiment. They can create different
layouts and see how the AI responds to each one.

4. Objectives

The main objective of Arena is to create a playable game that
demonstrates the use of Artificial Intelligence through multi agent
reinforcement learning.

The specific objectives of the project are:

develop a playable game environment using Unity.

create two teams of AI agents consisting of hiders and seekers.

use reinforcement learning to train the agents to improve their
behaviour through repeated simulations.

create a reward system that encourages hiders to remain hidden and
seekers to find or capture hiders.

allow the player to add objects and obstacles to the environment.

study how changes in the environment affect the behaviour of the AI
agents.

allow the AI agents to continue improving through multiple
generations of training.

create a simulation mode where the player can watch the agents
interact without directly controlling them.

display information such as team rewards, survival time, captures
and winning results.

allow players to compare the behaviour of agents from earlier and
later generations.

create an engaging game experience instead of presenting the
reinforcement learning model as a separate technical demonstration.

explore whether agents can develop different strategies when the
environment and opposing team behaviour change.

5. Justification

Artificial Intelligence in games is often created using fixed rules.
These systems are useful because they are simple and predictable, but
they can also make the behaviour of characters repetitive.

For example, if an enemy always follows the shortest path towards the
player, the player can learn this behaviour and use it to their
advantage. After some time, the game can become predictable.

Reinforcement learning provides a different approach. The agent can
learn from its previous actions and results. This can allow the agent to
improve without requiring the developer to manually program every
possible situation.

Multi agent reinforcement learning is especially useful for a game like
Arena because there are two teams with different objectives. The hiders
and seekers are not learning in isolation. Their actions affect each
other.

The environment also plays an important role. A wall can provide cover
for a hider. At the same time, the wall can make it harder for a seeker
to find the hider. If more walls are added, the agents may need to
change their movement and searching patterns.

This is where the player becomes an important part of the product.
Instead of simply watching a trained AI, the player can experiment with
the environment.

For example, the player can start with an open arena and observe the
agents. They can then add a few walls and run another simulation. After
that, they can create a more complex layout and see if the behaviour
changes.

The player can also compare different generations. Early generations may
show simple or inefficient behaviour, while later generations may show
more useful strategies.

The product can therefore provide an interactive way of understanding
reinforcement learning. The player does not need to understand the
technical details of the algorithm to see the result. They can simply
change the environment, run the simulation and observe what happens.

Another reason for choosing this project is that it combines AI with
game development. The final product will have a visual environment,
interactive controls and a simulation system. This makes the project
more suitable as an AI product rather than only a machine learning
experiment.

The project can also be extended in the future. More object types,
different maps, additional teams, different agent abilities and new game
modes can be added. The same basic system can be used to create
different situations for the agents.

The main goal is to create a product where AI is an important part of
the gameplay. The agents should not simply follow a set of fixed
instructions. They should be able to learn from their interactions and
change their behaviour over time.

Arena is therefore justified as an AI based game product because it
combines multi agent reinforcement learning, player interaction and game
simulation in one system. It provides a simple way for players to
experiment with an environment and observe how AI agents respond and
improve over time.
