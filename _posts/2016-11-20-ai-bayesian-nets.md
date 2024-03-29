---
layout: post
title: "AI/ML: Bayesian Nets"
date: 2016-11-20
sources: lecture, misc online sources
type: summary
---

## Why and How Do We Use Bayesian Networks?
Bayesian networks can represent probabilistic relationships between different variables. The network contains nodes, which represent random variables, and edges, which represent causal relationships between the variables. A Bayesian network contains the probability distributions of each variable in the network, conditioned upon the variables upon which a given variable depends. These conditional probabilities specify a joint distribution of the variables in the network. In this way, a Bayesian network can provide a compact representation of a probability distribution.

### Bayesian Networks Give a Compact Representation of Probability Distributions
Instead of storing the probability of every possible setting for each variable, we can just save the causality relationships and conditional probabilities of the variables in a Bayesian network. Using the relationships and conditional probabilities, we can compute the probability of each possible combination of states.

### Example
With this Bayesian network, we can compute joint probabilities involving whether it is raining, whether the grass is wet, and whether the sprinkler is turned on. 

![example Bayesian network](https://upload.wikimedia.org/wikipedia/commons/thumb/0/0e/SimpleBayesNet.svg/400px-SimpleBayesNet.svg.png) 

In this model, the state of the sprinkler depends only on whether it is raining or not, and the state of the grass (whether it is wet or not) depends on both the state of the sprinkler and whether it is raining. It gives the probability of rain, the probability that the sprinkler is on conditioned upon whether it is raining, and the probability that the grass is wet conditioned upon the state of the sprinkler and whether it is raining. Using this information, we can compute the probability of any given combination of variable states.
For example, P[raining, sprinkler on, grass wet] = P[raining] P[sprinkler on|raining] P[grass wet | sprinkler on AND raining] = (0.2)(0.01)(0.99) = 0.00198.
