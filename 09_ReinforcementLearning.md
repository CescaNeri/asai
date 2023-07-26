## Reinforcement Learning

Intelligence -> **goal-directed** adaptive behavior

Intelligence in Reinforcement Learning: *Learning to make decisions to achieve goals* 

An intelligent agent interacts with the **environment** by perceive an observation and take an action accordingly which leads to a **reward**.

Our goal is **maximizing** the sum of the rewards in the future.

### Reward hypothesis

Any goal can be formalized as the outcome of maximizing a cumulative reward.
Ideally we can formalize any problem as a reinforcement learning problem.

**Reward is enough**: intelligence, and its associated abilities, can be understood as subserving the maximization of reward by an agent acting in its environment.

There are several reasons why we should learn:

* Find solutions -> finite
* Adapt online (dealing with unknowns) -> continuous

RL is used in both cases, both episodic and continuing tasks. 
Adapting online is more challenging, and it is not just generalizations (!= from planning as the model is not known).

### Formalization

Reinforcement learning formalism includes:

* **Environment**: typically stochastic and unknown but STATIONARY (Markov Decision Process)
    - Stochastic: the next step is not fully determined
    - Stationary: if the probability distribution o the next state is the same for all time steps
* **Reward signal**: identifies what is good in the environment
* **Agent**: contains state and policy

### Sequentiality

Each time step t:

1. The agent receives an observation and execute an action
2. The environment receives the action
3. The agent-environment interaction ca be:
    - Episodic
    - Continuing

A full episode is a sequence of state-action-reward tuples (**trajectory**). RL follows the **Markovian property**, according to which the future is independent of the past given the present.
The environment can be either fully observable or partially observable.

### Reward

A reward is a scalar feedback signalS which describes how well the agent is doing.
The agent's sole objective is to maximize the **discounted cumulative** reward.
It can be of two types:

* **Sparse** (it can be null)
* **Dense** (we always have a reward which guides the agent toward the goal)

Immediate reward can be more important than future rewards.

### Agent Policy

The agent's behavior is determined by a **policy**. A policy is a mapping state to action (something that changes the environment).
Actions can be:

* Discrete
* Continuous

Policies can be:

* Deterministic
* Stochastic (to explore the environment)

The policy can be based on an estimation of the value function.

### Value

The value function gives the long-term value of the state under the policy. The value of a state is the total amount of reward an agent can expect to accumulate over the future, starting from the state.

The **state-action** value function gives a long-term value and allows me to maximize the return.

The optimal policy is the one that maximizes the expected return!

In RL, the policy is essential to explore the environment (exploration) while maximizing the **reward**.

*Epsilon Greedy Policy:* maximizes the return with probability 1 - e and acts randomly with probability e to explore the environment.

Exploration finds more information about the environment while exploitation exploits known information to maximize the reward.

*Exploration/Exploitation dilemma*

## Reinforcement Learning Problems

They can be of two types:

1. Tabular methods
2. Approximate methods (Deep RL)

The model is based on **policy iteration** to achieve the maximum reward and the maximum return.

Types of models:

* Value based (Q-Learning)
* Policy based (Reinforce)
* Actor critic (PPO)

### Q Learning

1. Initialize Q arbitrarily and put 0 on terminal states
2. For each episode:
    - Randomly initialize the state with t = 0:
        - For each step t:
            - Choose the action using a policy
            - Take the action and observe the reward
            -  Perform te update
            - Increase t

Q-Learning algorithms can be used both **Offline** and **Online**

### Offline

It creates a simulation of the selected environment, simulating the agent-environment interaction learning the Q-function.
However, there is no adaptation to the real environment and it may incur in the reality trap (the approximation of the environment is not good enough).

### Online

It learns the Q-function while interacting with the real environment evolves.