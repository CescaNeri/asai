## Auto ML

The increasingly growing size of data overcomes the availability of companies to analyze them.

AutoML smartly explores huge search spaces and regards the steps of data-preprocessing and modeling in the ML pipeline.

A data pipeline consists of a sequence of transformations.

### Auto Weka

Tool which allows for automated machine learning introducing **combined** algorithm selection and hyper-parameter optimization problems.

Elements:

* Data set
* Algorithms
* Hyper-parameters
* Metrics

Explore all the configurations is unfeasible, we need to explore a few of them bu
t in a smart way:

* Divide the exploration in iterations
* Keep track of past evaluation scores
* Build / update a probabilistic model

### Sequential Model-Based Optimization

It is a formalization of the Bayesian Optimization:

1. Evaluate some random hyper-parameters configurations
2. Build a probabilistic model
3. Exploit the model and the acquisition function to find the next hyper-parameters configuration to evaluate
4. Evaluate the hyper-parameters configuration
5. Update the probabilistic model incorporating the new results
6. Repeat steps 3-5 until the budget exceeded

### Meta Learning

It refers to the use of the results obtained in other case studies (according to meta-features) to tune other models.

`OpenML` -> online repository 

## Explainable Artificial Intelligence

Humans and intelligence agents work together in intelligent socio-technical systems to produce overall **intelligent behavior**.
Information and actions by intelligent agents need to be understandable by humans to be **accepted** and **trusted**.

**Symbolic** approaches are understandable by humans (transparent), but are slow, while **sub-symbolic** approaches are fast but opaque.

The solution is to join these two approaches.

### Local Interpretable Model-Agnostic Explanations (LIME)

It is a library which allows a clear and intuitive interpretation of prediction, applicable to any sort of supervised predictor.

### Explanations via Symbolic Knowledge Extraction

Any algorithmic procedure accepting trained sub-symbolic predictors as input and producing symbolic knowledge as output. 

## Multi Agent Reinforcement Learning

**Multiple agents** learn to take the right actions (policy) to maximize a **reward** signal.

AN agent does not have a perfect and complete knowledge of the state of the environment.
Environments are **partially observable** and changes over time.
Real-case environment dynamics could change over time and we loose convergence guarantees.

The goal is to find policies which works for an **unknown number** of agents.

* **Cooperative** (agents share the same reward function in order to accomplish a collective goal)
    - Homogeneous (each agent has the same capabilities)
    - Heterogeneous (each agent could have different capabilities)
* **Competitive** (agents compete with watch other to maximize a long term return)
* **Mixed** (agents can both compete and cooperate in order to maximize a global reward function)

Agents can learn in a centralized or decentralized way.
The goal is to find a centralized policy which works differently on each node.

### Rewards with Multi-Agent System

* A reward for each agent?
* A collective reward function?
* Combination?

The most efficient reward is give local rewards, which does not always work as it is not sure that the global goal will be achieve.

### Q Learning with Multiple Agents

Idea: each agent has its own Q table and each agent improves its Q table independently following a local policy.
 
 => Not feasable

Many agents systems are challenging environments for learning.
Solution: **Constraints**

### Mean-field Reinforcement Learning

Technique to reduce the complexity of a multi-agent system. The idea is to approximate the behavior of the agents.

### Field-Informed Multi-Agent RL

Technique that guides the learning process o the agents using a computational fields.
The idea is to ease the learning process.