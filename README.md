# Deep-RL-Stock-Portfolio-Management 

## Description 
This is an Reinforcement Learning agent using advantage REINFORCE (Baird 1994) to 
manage a portfolio in the stock market. 

For a detailed description, please see [this Devpost link](https://devpost.com/software/drl-for-automated-portfolio-management?ref_content=user-portfolio&ref_feature=in_progress)

The trained agent is able to learn a good policy and make profits compared to the 
general stock index. 

## Structure
> `agent.py` contains the advantage REINFORCE RL agent. This agent also uses 
>Experience Replay to stabilize training. 

> `main.py` contain training, validation, and testing 

> `preprocess.py` contains the pre-processing of financial data 

> `stock_env.py` contains the simulation environment of the stock market. This environment takes into
>account interest rate, inflation, ... It contains functions allowing the agent to 
>sample episodes of historical stock data using the agent's policy.

> `visual_helpers.py` contains helper functions to visualize the portfolio the agent is managing

> `rnn.py` contains a pre-trained Gated Recurrent Unit that can predict stock prices. 
>`rnn_model` contains a saved model of this GRU, and `data` contains the pre-processed data needed to train 
>this model. Ideally, this prediction made by this RNN is used as input to the RL agent, 
>although this feature is not implemented yet. 

## Running the model 
run the bash script `create_venv.sh` to create the virtual requirement for this model 
then run `python main.py` to start training and testing the model 
