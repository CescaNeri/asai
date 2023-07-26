## Intelligent Robotics Systems

Requirements for robotics systems:

* Be programmable by **learning** 
* Be able to predict **failure** states in their operating environment and their own bodies 
* **Plan** complex tasks
* Be able to deal with novelty, uncertainty and change (they should be **robust** and **adaptive**)

**Artificial Intelligence** can be a viable approach to robust design for reasoning, planning, learning, problem solving and behavior design.

A robot is an autonomous system which exists in the physical world, can sense its environment ans can act on it to achieve some goals.
Constituents of a robot:

* A physical body
* Sensors
* Effectors and actuators
* A controller

### Self Sufficiency 

Self-sufficiency means an agent's ability to sustain itself over extended periods of time.

* To be self-sufficient, complete agents must be able to perform multiple tasks
* Hence the problem of behavior control

**Autonomy** generally means 'freedom from external control'. Self-sufficiency increases the level of autonomy.
The extent to which an agent can control another depends on the controlling agent's knowledge of the state and internal mechanisms of the agent to be controlled.

*The capacity to learn increases autonomy*

**Adaptivity** is the ability ti adjust oneself to the environment: some property is maintained in changing environmental conditions via the modification of some element.

We can distinguish four types of adaptivity:

1. Evolutionary adaptation
2. Physiological adaptation
3. Sensory adaptation
4. Adaptation by learning

The behavior of an agent is always the result of the interaction with the environment.

### Behavior-based Robotics

* Roomba 

We want to program a robot so that it is able to explore an unknown environment avoiding collisions and being able to go to the recharging station when needed.

Examples of behaviors:

*  Avoid object
* Find an object
* Build a map
* Find a path 
* Hide from the light
* Aggregate with your team

Behaviors can be designed at a variety of levels of detail, with parallel execution and distributed control.
The network of behavior can store states can can be used to construct a model of the world. It can store history and look ahead into the future.
Behaviors are usually designed so that they operate on compatible time-scales.

*The best model that a robot can use is the world*

Behavior coordination can follow two methods:

1. Arbitration (competitive scheme)
2. Fusion (cooperative scheme)

### The Subsumption Architecture

Decompose robot architecture in task-achieving behaviors or **competences** with parallel and distributed control.


