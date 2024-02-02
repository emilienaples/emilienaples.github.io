---
layout: page
permalink: /nasa-jpl/
title: Motion Planning Under Uncertainty for Planetary Navegation
---

## NASA Jet Propulsion Laboratory <br />
### Robotics Research Deptartment <br/>
### Autonomous Systems Division

<br/>
<p>
The goal of this project was to enhance the Feedback Information Roadmap (FIRM) algorithm to account for both motion and sensing uncertainties to enhance motion planning capabilities for autonomous systems under extremely uncertain terrain and conditions. To approach this problem, I used POMDPs (Partially Observable Markov Decision Processes) as a way to maintain a sensor model, which represented the probability distribution of different observations in a robot’s environment.
These observations are mapped to actions through a belief state which captures the robot’s knowledge about its surroundings.
An exact solution to a POMDP then yields the optimal action for the robot over all states. </p>

- [Motion Planning Under Uncertainty for Planetary Navegation](/Notebooks/zUCR_PDF_version.pdf)


<img src="/images/diagram.png?raw=true"/>

<p> 
Problem: <br/>
Before, the algorithm only accounted for motion uncertainties. Decisions must be made about which action to take at each step or time point. The decision-maker or agent typically does not have full visibility of the true state of the environment (hence "partially observable"). Instead, they must rely on a set of observations that provide partial information about the state.</p>
<p>
Goal: <br/>
Improve the algorithm (math side) to account for sensing (sight) & the dimensionality problem, thus addressing the challenges of motion and sensing uncertainties. </p>

<p>
Solution:
Improve the FIRM algorithm (Feedback-based Information Roadmap) which updates the roadmap at each belief state. Doing so, the following improvements will be made: <br/>
- No need for expensive re-planning <br/>
- Still accounts for motion and sensing uncertainties <br/>
- Re-plans every time the localization module updates the probability distribution on the robot’s state </p>

<p>
Significant Applications: <br/>
Athena Rover <br/>
All future and upcoming Mars missions </p>


## How were POMDPs applied to address path planning under extreme uncertainty?
<br/>

By modeling the decision-making process as a partially observable environment: <br/><br/>
<p>
DEFINE THE STATES: Possible states of the environment, which include hidden information. <br/>
DEFINE THE OBSERVATIONS: The noisy and incomplete data received from sensors. <br/>
DEFINE THE ACTIONS: Possible movements and decisions the rover can take. <br/>
DEFINE THE REWARDS: The system's objectives, such as reaching a destination while avoiding obstacles. <br/>
</p>

<img src="/images/POMDP.png?raw=true"/>

The POMDP is modeled as follows: <br/>

A 6-tuple (S, A, O, T, Z, R): <br/>
S: State space (set of all possible states the system can be in) <br/>
A: Action space ( set of all actions that the decision maker can take) <br/>
O: Observation space (set of all possible observations that the decision maker can make about the actual state of the system) <br/>
T: Transition function (deffines the probability of transitioning from one state to another state given a particular action) - T(s, a, s’) = P(St+1 = s’ | St = s, At = a) <br/>
Z: Observation function (gives the probability of making an observation given a state of the system and an action that has been taken.) <br/>
<br/>
Z(s, a, o) = P(Ot+1 = o | St+1 = s, At = a) <br/>
<br/>
R(s, a): Reward function (assigns a numerical reward to each action taken in a particular state) <br/>

Additionally, a policy (action selection strategy) also defines the action to take in each state. The policy maps each 
belief state s to an action → a. <br/><br/>

<p>
The progression of states (S0, S1, S2, etc.), observations (O0, O1, O2, etc.), actions (A0, A1, A2, etc.), and rewards (R0, R1, R2, etc.) over time. This kind of diagram is typically used to visualize the dynamics of a POMDP, where at each time step, an action is taken based on the current belief state, a new observation is made, and the belief state is updated. 
<p>
We are then able to make decisions with incomplete knowledge about the current state and where the outcomes of actions are uncertain. </p>

