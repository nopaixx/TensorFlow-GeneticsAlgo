# TensorFlow-GeneticsAlgo GA
Optimize TF layers weigth with Genetics Algorithms

Gradient descending agorithm are well known for optimizing the weights of neural networks and finding the solution to converge into an optimal solution.

Usually the derivative is applied to a single output value and then the decision is gradually improved through an improvement in the optimization function (or target). 

The purpose of this mini-project is to demonstrate that we can optimize the weights of a net in TensorFlow (keras) using a basic genetic algorithm initiated from a random state.


# About Genetics Algorithms

Genetic algorithms are based on the genetic process of biologically living organisms. Where in a closed environment of X species only the strongest or the best adapted to the environment survive in a new species to evolve to a new being through the genetic mixture of the survivors.

# Basic concepts about GA

Genes->Parameter to be optimized

Species->Each species contains a certain amount of genes all together offer a solution to a specific problem.

Population-->Population is a group of species all together perform a generation

Evolution->Evolution is the step that is generated between one generation and another, where there is a mixture of genes that generates new species and new species are born with a certain mutation.

![alt text](https://github.com/nopaixx/TensorFlow-GeneticsAlgo/blob/master/GA%20grafic.jpg)

# Where it is useful to apply genetic algorithms?

There is a varied range of problems to which the application of genetic algorithms can be useful between them if we want to optimize the weights of a neural network. For practical purposes, it is especially useful when the train dataset could be diferent at each step specially if we want to teach a network to make full decisions based on past decisions(outputs) of the same network.

# Can we teach a network to drive a car? 
For example the network receives inputs from distance sensors to an obstacle and the network can make several decisions (braking, turning, accelerating etc.). We must bear in mind that each observation in the train dataset is completely dynamic because each observation the distances of the sesons will be different based on the past decisions of the network.


# Can we teach a network to deploy a full (and unkown) Financial Stocks Maket strategy.
Usually quantitave traders download financial timeseries then apply a treatment to the data if necessary (normalization PCA etc...). Finally they train a network(python/R etc..) normally with the objective of reducing the error between the prediction and the real value and finally they take a decision(automatic or not) based on model prediction.

Please note that the main problem quantitative traders face when training a network with static observations for the financial markets are completely exposed to high volatility, which is why most quantitative traders lose they money. They not only need a predictive model of a value but they also need a complex and operative system that is able to manage the capital effectively.

Theoretically and as demonstrated by google with the Alpha Zero version the system can learn in a more efficient way (and sometimes surprisingly) if it is not conditioned by human knowledge itself.

This is with genetic algorithms we can train a network to make complex decisions such as (buy,sell, parcial close, hedges etc..) all based on the current state of command control of the trading platform.
(FOR MORE INFORMATION ABOUT FIANACIAL STOCK WITH GENETICS ALGORHITMS PLEASE READ Project https://github.com/nopaixx/MaketsGA)



# About train.py 
For easy implementation code we have based ourselves on the kaggle competition TAG SALT IDENTIFICATION (https://www.kaggle.com/c/tgs-salt-identification-challenge)

Pay attention to:

-def parallel_scoring ->Perform a custom fitness funcion higher value best

-def runtournament ->Perform a random natural seleccion of two best species to join

-def model_crossover  ->Join best two species in random way and apply a muttation

-Check not model.fit() transaction is executed at any time

# Conclusions

-As main objective of the document we have been able to optimize a neural network (in the case of the example Convultional) without applying the method of Gradient descen.

-We have talked about how we can use genetic algorithms to train neural networks and how we can use neural networks from a different point of view.

-No doubt about the use of GA in neural networks presents an advantage for certain types of problem in which for example the traing set observations are dynamic and varied in each training episode

-I think this may be the beginning of a more complex and optimized library to develop advanced quantitative trading models where the predictive model does not consist of a buy or sell signal in itself, but the model consists of a complex trading system in itself.


 
