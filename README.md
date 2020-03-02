# Stock-Trading-with-Reinforcement-Learning
### Stock trading environment

RL takes action in the provided environment that we are going to describe.
We are going to study how a RL algorithm might take an action in a stock trading environment.
What makes this a RL problem is a matter of perspective.
We try to follow the rule `buy low` and `sell high`.

### Data and environment


Because will work historical stock data, this is a simulation. We will figure out how to build an environment object in code that simulate this stock market.
The questions we will consider are:

#### `What are the state variables?`

We will borrow some ideas from `practical Deep Reinforcement Learning`. State will consist of 3 parts:

- How many share of each stoke I own

- Current price of each stock

- How much cash we have

We can think of it like a time series problem look at the pattern we have built in the past and from now make a decision.
#### `Do we have enough cash to buy stocks we want to buy?`

If we have `N stocks` then the state will contain `2N+1` components.

#### `What are the actions?`

* Many options to consider

* For any stock, I can buy/sell/hold

* In our environement, we will have 3 stocks to consider then we will have `3*3*3 = 27 possibilties`

#### `What is the reward?`

- Change in value of portfolio one step (state `s`) to the next (state `s'`)

- How we will calculate the value of the portfolio

#### Portfolio Value

Reward is just the change in portfolio value between steps.

`s = vector of shares owned`

`p = vector of share prices`

`c = cash`

`portfolio value =  s*p + c`






