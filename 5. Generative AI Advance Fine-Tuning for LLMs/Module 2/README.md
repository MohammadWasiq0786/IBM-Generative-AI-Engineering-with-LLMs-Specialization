# Summary and Highlights 

Congratulations! You have completed this module. At this point in the course, you know the following: 

* The reward function provides human feedback for the inserted query.
* Rollouts help queries and responses to review the sampling process. The rollout libraries, such as Hugging Face, differ from the reinforcement learning.
* The expected rewards use an empirical formula to understand how an agent performs in the language model.
* Reinforcement learning from human feedback (RLHF) uses response distribution as an input query to fine-tune the pre-trained LLMs.
* Pre-trained reward model evaluates and generates a reward for the query plus response.
* Proximal policy optimization (PPO) provides feedback on the quality of actions taken by the policy.
* The sentiment analysis pipeline scores evaluate the generated responses' quality. Pipe_outputs list generates scores for the responses.
* The LengthSampler varies text lengths for data processing, enhances model robustness, and simulates realistic training conditions.
* The sample query questions may provide various random responses based on the probability distribution. 
* The transformer model generates probabilities for different words using the softmax function. 
* You can select words at various timestamps and change the probabilities for those words.
* The generation parameters, such as temperature, top-k sampling, beam search, top-p sampling, repetition penalty, and max and min tokens, help change the sequences generated using LLMs.
* Objective functions coordinate algorithms and data to reveal patterns, trends, and insights to produce accurate predictions. They measure the difference between an ML model’s predicted outcomes and target values.
* The Kullback-Leibler, or KL, divergence measures the difference between two probability distributions, the desired and the arbitrary policy.
* The optimal solution scales the reference model to the reward function, with the beta parameter controlling the constant.
* Following the policy distribution, the language model generates responses based on the inserted query.
* The policy gradient method maximizes the objective function, and PPO helps to achieve this maximization.
* To optimize the policy, derive the sample response, estimate the reward, and extend the dataset.
* You can calculate the log derivative by identifying a policy that maximizes the objective function by simplifying the expression and converting it into analytical distributions. 
* Use a toy gradient ascent example using stochastic gradient ascent or SGA to maximize the objective function compared to a standard optimization problem with maximum likelihood.
* A positive update occurs when a reward is positive, and a negative update occurs when a reward is negative.
* To train the model, regularly evaluate it using human feedback, use the moderate beta value, and increase the temperature.
  

* Direct Preference Optimization (or DPO) is a reinforcement learning technique designed to fine-tune models based on human preferences more directly and efficiently than traditional methods.
* DPO involves collecting data on human preferences by showing users different outputs from the model and asking them to choose the better one.
* DPO involves three models: the reward function, which uses an encoder model, the target decoder, and the reference model.
* In DPO, you can convert a complex problem into a simpler objective function that is more straightforward to optimize.
* Two main steps to fine-tuning a language model with DPO:
  * Data collection 
  * Optimization
* Steps to fine-tune a language model with DPO and Hugging Face:
  * Step 1: Data preprocessing
    *  Reformat
    *  Define and apply the process function
    *  Create the training and evaluation sets
  * Step 2: Create and configure the model and tokenizer
  * Step 3: Define training arguments and DPO trainer
  * Step 4: Plot the model's training loss
  * Step 5: Load the model
  * Step 6: Inferencing
* DPO leverages a closed-form optimal policy as a function of the reward to reformulate the problem
* Reward policy:

$$\pi_r(Y|X)= \frac{\pi_{ref} (Y|X) exp \big(\frac{1}{\beta} r(X, Y) \big)}{Z(X)}$$

* Subtracting the reward model for two samples eliminates the need for the partition function

$$r(X. Y_{w})- x(X, Y_l)= \beta \quad ln\Big(\frac{\pi_r (Y_w|X)}{\pi_{ref} (Y_w|X)} \Big)- \beta \quad ln\Big(\frac{\pi_r (Y_l|X)}{\pi_{ref} (Y_l|X)} \Big) $$

* Loss function:

$$ - \sigma \Bigg( \beta \quad ln\Big(\frac{\pi_r (Y_w|X)}{\pi_{ref} (Y_w|X)} \Big)- \beta \quad ln\Big(\frac{\pi_r (Y_l|X)}{\pi_{ref} (Y_l|X)} \Big) \Bigg) $$
