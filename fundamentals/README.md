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


 
Open question: 1) How to make multi model RL systems ?  2) Could such systems learn more quickly than the systems that purely rely on systematic information ? 

