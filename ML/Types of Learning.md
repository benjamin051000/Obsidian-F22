Machine Learning algorithms fall into one of the following categories:

## Supervised Learning
Model learns from labeled data

You must:
- Collect data
- Label the data

## Unsupervised Learning
Model learns from unlabeled data

You must:
- Collect data

- Algorithm labels the data itself

## Semi-Supervised
- Collecting and labeling data takes a long time
- Semi- labels some data, not all of it 

## Reinforcement Learning
System takes action based on reward or penalty

Example: Robot has goal to vacuum the house without hitting any walls
- System uses inputs (vision)
- Move around house without hitting stuff
- If it hits a wall, add a penalty
	- Now it will learn to not do that anymore
- Very popular in robotics

# Other types
## Multiple Instance Learning
Model will learn based on multiple-instance labels that have a particular form of imprecision

## Active Learning
(type of supervised learning)
Model learns by obtaining labels online from user/oracle in intelligent fashion

## Transfer Learning
Transfer learnt knowledge from similar previous task


# Supervised Learning
Example: Distinguish between two types of birds.

## Classifiers
### Discriminative vs Generative
![[Discriminate vs Generative Classifications]]

Law of total probability:
$$ P(x) = P(x|C_0)*P(C_0)+P(x|C_1)*P(C_1) $$

## Regression
- Predictive modeling approach
- Continuous outputs
- Example: Determine the age of a person by their silhouette.


## Typical flowchart for supervised learning

![[Types of Learning 2022-08-25 15.25.42.excalidraw]]
Use a **learning algorithm** to explore the solution space!

E.g., *gradient descent*: $-\nabla J(w_0)$

Optimize for the parameters (the $w$ s!) by training the model.

## Testing phase
Test data: $x$ -> Features $\phi(x)$ -> Prediction with trained mapper: $f(\phi(x),w^*)$

Tune something called hyperparameters to help tell if the training is working correctly

