# Ingredients
1. Good exploration, function approximation, planning to revisit areas already explored
2. Reward function to incentivize/dis-incentivize behaviors

Differences between supervised learning, unsupervised learning, and reinforcement learning?
* **Supervised learning** We assume the learner has access to labeled examples giving the correct answer.
* **Reinforcement Learning** The reward gives the agent some idea of how good or bad its recent actions were.
  *   You can think of supervised learning as requiring a teacher that helps you by telling you the correct answer.
  *   A reward on the other hand, is like having someone who can identify what good behavior looks like but can't tell you exactly how to do it.
* **Unsupervised learning** is about extracting underlying structure in data. It's about the data representation

# Sequential Decision Making
Key terms, in the example below a doctor is running a trial of (k=3) different medicines and monitoring patient outcomes
- Doctor is the agent taking actions
- Assigning a particular medicine to a patient is an action, there are 3 different medicines indicating 3 different actions
- Patient's health after getting the medicine is the outcome from the action
![Screenshot 2024-06-05 at 2 23 08 PM](https://github.com/unnitin/reinforcement-learning/assets/14156349/b29d9f97-f46f-4067-bacc-f34e3b667dca)

## Estimating Action Value 
1. **Sample average method**     
In the screenshot below, $Q*$ is not known to the user 
![Screenshot 2024-06-10 at 8 29 05 PM](https://github.com/unnitin/reinforcement-learning/assets/14156349/bbfb3a57-e2df-459e-9c91-a68864b228c5)

In an example scenario, the doctor runs a trial randomly assigning the drug to patients and recording the outcome (0,1 - failure, success) 
 * As the trial progresses, estimates of `action value` approach $Q*$
![Screenshot 2024-06-10 at 8 38 16 PM](https://github.com/unnitin/reinforcement-learning/assets/14156349/11814536-0849-495e-aa21-e9fc519fc12d)

2. **Estimating sample average incrementally**
 * Useful in cases where we are supporting an online experiment and data will accumulate overtime
 * $NewEstimate = OldEstimate + \alpha (Target - OldEstimate)$      
 * *NewReward* at time step *t* is the target for that timestep
 * $\alpha$ is the step size in the general update case, for sample average method it is 1/n where n is the number of steps taken

## Using Action Values to determine next action
Exploration v/ Exploitation - Broadly in `Reinforcement Learning`, we need to balance between exploration where we explore pay-off from different actions to understand their action-value distribution and exploitation where we use our estimated action-value distributions from different actions at any given point to take the best. Few methods that help balance this trade-off are listed below ... 
1. **Epsilon-Greedy action search** Epsilon ($\varepsilon$) refers to the probability of exploring option space, we exploit with probability 1 - $\varepsilon$
   * If there are ties at the exploit step, they are broken randomly
3. **Optimistic Initial values** Encourages early exploitation as the initial estimate is significantly higher than the true estimated reward, the algorithm chooses to explore a lot early as a result
4. **Upper Confidence Bound Interval** We select actions with most uncertainity in their estimates
   * The idea is that this incentivizes exploration to get the uncertainity in action-value distributions down over time
   * Following formula is used to determine the action to be taken, $A_t = argmax(Q_t(a) + c \sqrt{\ln(t) / N_t(a)}$
   * c is a user-specified parameter that controls weightage to upper bound of the estimate
   * t is total time steps, $N_t(a)$ is total time steps for action `a`
   * Note how uncertainity term is inversely proportional to $N_t(a)$
   * $Q_t(a)$ controls exploitation, second term controls exploration
   * Method does not deal with non-stationary problems very well as in those cases the uncertainity in estimates can change over time 

## Lorem Ipsum
$x + y$     
$\Gamma$     
$\coloneqq$

Open question: 1) How to make multi model RL systems ?  2) Could such systems learn more quickly than the systems that purely rely on systematic information ? 

