---
layout: post
include: true
title:  "Relations between Mutual information, Cross entropy, KL Divergence"
excerpt: "Quantizing the relations between two random variables and distributions"
date:   2020-06-02 10:00:00
mathjax: true
---

* TOC
{:toc}

### The intutive definition of Mutual Information

Mutual information is the measure of **reduction in the uncertainity** about one quantity (a random variable), that is achieved *by observing another quantity* (another random variable).
**_Take for example :_** A car moving with certain velocity(say $$v_s$$) which is given by its on board sensor(A noisy speedometer), and there is a GPS receiver on the car which measures 
rate of change of position (velocity of the car) say $$v_g$$, now since there is some process ans measurment noise, we can say $$v_s$$ and $$v_g$$ are random variables, now the 
mutual information between these two, quantifies the reduction in uncertainity about $$v_s$$, given $$v_g$$.<br/>
If the two random variables $$v_s$$ and $$v_g$$ are independent, the mutual information between them is zero. i.e. $$v_s$$ and $$v_g$$ don't share any information.
### Let's discuss some mathematical discription and few other terms
**Conditional Entropy $$H(v_s|v_g)$$:**<br/>
It is the amount of information gained, once the outcome of v_s is known, given the outcome v_g <br/>
**Joint Entropy $$H(v_s,v_g)$$ :**<br/>
It is the entropy of joint distribution of two random variables.<br/>
<br/>
Let us denote Mutual information with $$I(v_s, v_g)$$ ,<br/>
$$I(v_s, v_g) \, = \sum \, p(v_s, v_g) \, \log_{2}\dfrac{p(v_s,v_g)}{p(v_s)p(v_g)}$$<br/>
let, $$H(.)$$ denote the Shanon's Entropy function<br/>
$$I(v_s, v_g) \, = \, H(v_s)\, - \, H(v_s|v_g) = H(v_g)\, - \, H(v_g|v_s) = H(v_s)\, + \,H(v_g) \, - \, H(v_s,v_g)$$ 
### Mutual information and KL divergence
KL divergence between any two random variable **distributions** tells us about, how different are the two distributions.
Mutual information tells us how much information one random variable contains, about another random variable.
**_one thing to always remember:_** lower the uncertainity, lower the information (Recall Claude Shannon's, definition of Information).<br/>
> Now, think for few minutes about relating these two (Hint: Use the mathematical description of mutual information and Kl divergence)<br/>
<br/>
**The KL divergence $$(D_{KL}(p||q))$$:**<br/>
The KL divergence between two probability distributions P and Q is,<br/>
$$D_{KL}(P||Q)\, = \, \sum p\,\log_{2}\, \dfrac{P}{Q}$$ <br/>
<br/>

Therefore, the Mutual information is the KL divergence between joint distribution and product distribution(The joint distribution if the two random variables were independent) of $$v_s$$  and $$v_g$$
i.e. $$ I(v_s, v_g) \, = \, D_{KL}(p(v_g,v_s)\,||\, p(v_g)p(v_s)) $$, this obvious by comparing the definitions of  Mutual information and KL Divergence.<br/>

>KL divergence is also know as **relative entropy**<br/>
>But, why?<br/>
<br/>
Before proceeding with the answer, we must go through one more term i.e. The **cross entropy**<br>
**Cross Entropy $$H(P,Q)$$:**<br/>
When the true distribution $$P$$ is unknown, the encoding of random variable can be based on another distribution $$Q$$ as a model that approximates $$P$$. 
Then the average of the total number of bits needed to represent it, is called the cross-entropy.<br/>
$$H(P,Q)\,=\,\sum_i\,P_i\,\log_2\,\dfrac{1}{Q_i}$$<br/>

**Cross Entropy = KL divergence + Enropy** i.e.$$H(P,Q) \,=\, D_{KL}(P||Q)\, - \,H(P)$$<br/>

>Therfore, KL Divergence is the difference between Cross entropy and entropy<br/>
>Hence, KL divergence is also called as Relative entropy<br/>
<br/>


### Why is Mutual information, KL Divergnece important



#### Deep think !!!
1.Since mutual information is relating one random variable distribution with other, is there any relation between **importance sampling** and **Mutual information**?