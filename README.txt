DICE GAME

The dice game can be modelled as a Markov decision process because the reward
and new state (dice combination) after each roll depend only on the previous
state and action. Modelling the dice game as a Markov decision process, I used
value iteration to create my agent.

Value iteration is used to try and find the optimal policy for the agent.
The optimal policy dictates which action should be taken from each state to
achieve the best reward. I started by assigning an arbitrary value of 0 to each
best possible state value, and then used the Bellman equation to recursively 
update the best possible value for each state after trying each action, and 
documenting  which action led to the best value each time. I repeated this 
process until either an iteration limit of 1000 had been reached, or the values 
had converged to a 'sufficient' degree. I chose theta = 0.000005 to be a 
sufficient figure for convergence. The value for gamma in the recursive
equation should be chosen based on how much the agent values future reward.
After trial and error I found that gamma = 0.6 produced the highest rewards. Both
my iteration limit value and value for theta were also chosen based on trial and
error.

Given more time, I would have tried implementing policy iteration. While both
value iteration and policy iteration will find an optimal policy eventually, an
algorithm using policy iteration will converge with fewer iterations and should
therefore be a faster way of finding the optimal policy.
