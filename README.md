# Stockprice-prediction-using-reinforecment-learning





### Introduction

“The share price of JPMorgan Chase is going up. It’s on an increasing trend. People are selling their stocks and making money.”

These statements are commonly heard in today's stock market. The stock market presents an opportunity for earning and investing money. However, it can also evoke greed and prompt individuals to make drastic decisions due to its highly volatile nature. Investing in stocks involves a gamble where one can experience either profit or loss. It's important to note that there is no definitive prediction model for stock prices, as their movement is primarily influenced by the demand and supply ratio.

### Goals

This project aims predict stock prices by employing reinforcement learning as a solution. We will delve into the various reinforcement learning techniques that have been utilized in predicting stock market behavior.


### What is Reinforcement Learning?

Reinforcement learning, in addition to supervised and unsupervised learning, is another category of machine learning. Unlike supervised learning, reinforcement learning operates on an agent-based learning framework, where the agent interacts with an environment to maximize its performance. Unlike supervised learning, reinforcement learning does not rely on labeled data.

Reinforcement learning demonstrates effectiveness even when limited historical data is available. It leverages the value function, which is calculated based on the policy determined for each action.
	
Reinforcement learning is modeled as a Markov Decision Process (MDP):

•	An Environment E and agent states S

•	A set of actions A taken by the agent

•	P(s,s’)=>P(st+1=s’|st=s,at=a) is the transition probability from one state s to s’

•	R(s,s’) – Immediate reward for any action




### How can we use reinforcement learning to predict stock market prices? 

Reinforcement learning can be employed to predict the price movements of a particular stock by leveraging its core principles, such as the ability to work with limited historical data and operate within an agent-based system to anticipate higher returns in the prevailing market conditions. In this project, we will explore an example of stock price prediction for a specific stock using a reinforcement learning model, with a focus on understanding the underlying concept of Q-learning.


The process of designing a reinforcement learning model involves the following steps:

1.	Importing the necessary libraries for the task.
3.	Creating an agent that will make all the decisions.
4.	Defining essential functions for value formatting, sigmoid function implementation, reading data files, etc.
5.	Training the agent using appropriate algorithms and techniques.
6.	Evaluating the performance of the agent based on predefined metrics and criteria.



### Defining the Reinforcement Learning Environment

MDP for Stock Price Prediction:

Agent – An Agent A that works in Environment E

Action – Buy/Sell/Hold

States – Data values

Rewards – Profit / Loss



### Q – Learning

Q-learning is an algorithm for reinforcement learning that operates without a predefined model, allowing an agent to learn the quality of different actions and determine the appropriate action to take based on specific circumstances. By maximizing the expected value of the cumulative reward over subsequent steps, starting from the current state, Q-learning identifies an optimal policy.


### Gathering Data

1.	Open Yahoo Finance 
2.	Enter the name of the desired company, such as JPMorgan Chase.
3.	Choose the desired time period, such as last one year.
4.	Click on the "Download" button to initiate the CSV file download.



 






### Implementing the Model in Python



#### Creating Agent

The code for creating the agent starts with initializing various parameters. Several static variables such as gamma, epsilon, epsilon_min, and epsilon_decay are defined. These constants serve as thresholds that guide the buying and selling process for stocks and help maintain the parameters within a certain range. These minimum and decay values function as thresholds in a normal distribution.

The agent constructs a layered neural network model to determine whether to buy, sell, or hold stocks. It makes decisions based on previous predictions and the current state of the environment. The "act" method is used to predict the next action to be taken. In case the memory becomes full, there is another method called expReplay designed to reset the memory.

 

#### Defining Basic Functions

1.	The formatprice() function is implemented to standardize the currency format.
2.	The getStockDataVec() function is used to import the stock data into Python.
3.	Sigmoid function is defined as a mathematical calculation to transform values.
4.	The getState() function is written to provide the current state of the data.


#### Training the Agent

Based on the action predicted by the model, the buy/sell operation adds or deducts money accordingly. The training process involves multiple episodes, analogous to epochs in deep learning. Finally, the model is saved for future use.

In this case we are training the model with stock prices of JPMC Bank from May 2022 till March 2023




#### Evaluation of the model

After training the model using new data, its performance is assessed by conducting tests to determine the profit or loss generated by the model. This evaluation process allows gauging the reliability and effectiveness of the model in making predictions. 

To evaluate the model, we use stock prices from March ’22 till May ’22 to see what the profit could be per stock and the profit if we traded 100 units of stock 

 

### Conclusion
Stock predictions using reinforcement learning is yielding positive results, showcasing the potential of Q-learning through various experimental approaches. Further exploration and advancements in reinforcement learning research will enhance its application and instill greater confidence in its capabilities.





### References: 
[1] Mnih, V., Kavukcuoglu, K., Silver, D., Rusu, A. A., Veness, J., Bellemare, M. G., ... & Petersen, S. (2015). Human-level control through deep reinforcement learning. Nature, 518(7540), 529-533.
[2] Shah, E. (2020). Predicting Stock Prices using Reinforcement Learning [Blog post]. Retrieved from [https://www.analyticsvidhya.com/blog/2020/10/reinforcement-learning-stock-price-prediction]
[3] Xiong, Z., Liu, D., Wu, S., & Bai, Q. (2018). Stock price prediction based on reinforcement learning algorithm. International Journal of Intelligent Computing and Cybernetics, 11(1), 78-95. [4] Guo, C., Zhang, J., Yang, Z., & Yu, Y. (2017). Deep reinforcement learning for trading. In Proceedings of the 34th International Conference on Machine Learning-Volume 70 (pp. 1323-1332). JMLR. org.
![image](https://user-images.githubusercontent.com/124342508/236711580-b086d11b-439d-449f-bf7b-9e1b3f346dbb.png)
