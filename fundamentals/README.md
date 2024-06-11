# Ingredients
1. Good exploration, function approximation, planning to revisit areas already explored
2. Reward function to incentivize/dis-incentivize behaviors

Differences between supervised learning, unsupervised learning, and reinforcement learning?
* Supervised learning: We assume the learner has access to labeled examples giving the correct answer.
* RL: The reward gives the agent some idea of how good or bad its recent actions were.
  *   You can think of supervised learning as requiring a teacher that helps you by telling you the correct answer.
  *   A reward on the other hand, is like having someone who can identify what good behavior looks like but can't tell you exactly how to do it.
* Unsupervised learning is about extracting underlying structure in data. It's about the data representation

## Sequential Decision Making
Key terms, in the example below a doctor is running a trial of (k=3) different medicines and monitoring patient outcomes
- Doctor is the agent taking actions
- Assigning a particular medicine to a patient is an action, there are 3 different medicines indicating 3 different actions
- Patient's health after getting the medicine is the outcome from the action
![Screenshot 2024-06-05 at 2 23 08 PM](https://github.com/unnitin/reinforcement-learning/assets/14156349/b29d9f97-f46f-4067-bacc-f34e3b667dca)

### Estimating Action Value 
1. Sample average method - in the screenshot below, $Q*$ is not known to the user 
![Screenshot 2024-06-10 at 8 29 05 PM](https://github.com/unnitin/reinforcement-learning/assets/14156349/bbfb3a57-e2df-459e-9c91-a68864b228c5)

In an example scenario, the doctor runs a trial randomly assigning the drug to patients and recording the outcome (0,1 - failure, success) 
* As the trial progresses, estimates of `action value` approach $Q*$
![Screenshot 2024-06-10 at 8 38 16 PM](https://github.com/unnitin/reinforcement-learning/assets/14156349/11814536-0849-495e-aa21-e9fc519fc12d)

2. Estimating sample average incrementally     
$NewEstimate = OldEstimate + 1/n(Target - OldEstimate)$
New Reward at time step t is the target for that timestep

### Using Action Values to determine next action
1. Greedy action search

## Methods to balance exploration and exploitation
$x + y$     
$\Gamma$     
$\coloneqq$

Open question: 1) How to make multi model RL systems ?  2) Could such systems learn more quickly than the systems that purely rely on systematic information ? 

