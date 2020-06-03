---
layout: post
include: true
title:  "Relations between Mutual information, Cross entropy, KL Divergence"
excerpt: "none"
date:   2020-06-02 10:00:00
mathjax: true
---

* TOC
{:toc}

### The intutive definition of Mutual Information

Mutual information is the measure of ** reduction in the uncertainity ** about one quantity (a random variable), that is achieved * by observing another quantity * (another random variable).
**_ Take for example : _** a Car moving with certain velocity(say $$v_s$$) wich is given by its on board sensor(A noisy speedometer), and there is a GPS receiver on the car which measures 
rate of change of position (velocity of the car) say $$v_g$$, now since there is some process ans measurment noise, we can say $$v_s$$ and $$v_g$$ are random variables, now the 
mutual information between these two, quantifies the reduction in uncertainity about $$v_s$$, given $$v_g$$
 
### Why is Mutual information important and Maximally informative dimentions 

### Mutual information and KL divergence
KL divergence between any two random variable distributions tells us about, how different are the two distributions.
Mutual information tells us how much information one variable contains, about another random variable._one thing to always remember:_ lower the uncertainity, lower the information (Recall the honorable Claude Shannon's, definition of Information). 
................
Now, think about relating these two(Hint: Use the mathematical description of mutual information, Kl divergence and Cross Entropy)
.....More to come just getting stated, will come back soon
#### Deep think !!!
1. Since mutual information is relating one random variable distribution with other, is there any relation between **importance sampling** and **Mutual information**?