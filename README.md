# nim-AI-Game

The AI used in this game is a Reinforcement Learning (RL) agent based on Q-learning, which is a type of model-free reinforcement learning algorithm.

This AI relies on tabular Q-learning, which is effective for small state spaces like the Nim game.


## Key AI Features in the Code:
Q-learning:

        The AI maintains a Q-table (self.q), which stores state-action values.
        It updates the Q-values based on rewards received from game outcomes.
        
Exploration vs. Exploitation:

        The AI chooses actions using an ε-greedy strategy:
            With probability epsilon, it selects a random action (exploration).
            Otherwise, it picks the best-known action based on Q-values (exploitation).
            
Learning Process:

        The AI plays games against itself (train(n)) to improve its strategy.
        It updates Q-values using:
        Q(s,a)=Q(s,a)+α[(r+max⁡Q(s′))−Q(s,a)]
        Q(s,a)=Q(s,a)+α[(r+maxQ(s′))−Q(s,a)] 
        where:
            α (alpha) is the learning rate.
            r is the reward.
            max Q(s') is the best future reward from the next state.
