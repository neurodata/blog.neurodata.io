---
layout: post
title:  "The Varieties of Hypothesis Tests"
date:   2018-09-29 14:27:57 -0400
tags: bits
author: Joshua Vogelstein
---

Hypothesis testing is a procedure for evaluating the likelihood that a given dataset corresponds to a particular "null" model.   Formally, all hypothesis testing scenarios can be described as follows.


Let $$X_i \sim F$$, for $$i \in [n]=\{1,\ldots,n\}$$ be a random variable, where each $$X_i$$ is sampled independently and identically according to some distribution $$F$$.  Realizations of $$X_i$$ are $$x_i \in \mathcal{X}$$.  We further assume that $$F \in \mathcal{F}$$, that is $$F$$ is a distribution that lives in a model $$\mathcal{F} = \{F : \mathcal{F}\}$$.  Moreover, we partition $$\mathcal{F}$$ into two complementary sets, $$\mathcal{F}_0$$ and $$\mathcal{F}_A$$, such that $$\mathcal{F}_0 \cup \mathcal{F}_A = \mathcal{F}$$ and $$\mathcal{F}_0 \cap \mathcal{F}_A = \emptyset$$.  Given these definitions, all  hypothesis testing can be written as:

\begin{align}
H_0: F \in \mathcal{F}_0, \qquad
H_A: F \in \mathcal{F}_A.
\end{align}


<!-- For example, $$\mathcal{F}$$ could be the set of all Gaussians, and therefore $$x_i \in \mathbb{R}$$, and $$\mathcal{F}_0$$ could be $$\mathcal{N}(0,1)$$, and $$\mathcal{F}_A=\mathcal{N}(1,1)$$.    -->

Note that a hypothesis can be either *simple* or  *composite*: according to [wikipedia](https://en.wikipedia.org/wiki/Null_hypothesis), simple hypothesis tests are
"any hypothesis which specifies the population distribution completely," whereas composite tests are "any hypothesis which does not specify the population distribution completely." Given this, we consider four different kinds of hypothesis tests:


1. Simple-Null, Simple-Alternate (S/S)
\begin{align}
H_0: F = F_0, \qquad
H_A: F = F_A.
\end{align}

2. Simple-Null, Composite-Alternate (S/C)
\begin{align}
H_0: F = F_0, \qquad
H_A: F \in \mathcal{F}_A.
\end{align}

2. Composite-Null, Simple-Alternate (C/S)
\begin{align}
H_0: F \in \mathcal{F}_0, \qquad
H_A: F \in \mathcal{F}_A.
\end{align}

3. Composite-Null, Composite-Alternate (C/C):
\begin{align}
H_0: F \in \mathcal{F}_0, \qquad
H_A: F \in \mathcal{F}_A.
\end{align}

Each of the above can be re-written in terms of parameters.  Specifically, we can make the following substitutions:

\begin{align}
F = F_j \Rightarrow \theta(F) = \theta(F_j),  \qquad
F \in \mathcal{F}_j \Rightarrow \theta(F) \in \Theta_j,
\end{align}
 where $$\Theta_j = \{ \theta : \theta(F) \in \mathcal{F}_j \}$$.

Note that composite tests (those where the null or alternate is composite) can be both one-sided or two-sided.  In particular, the simple/composite null hypothesis can be restated: $$H_0: F-F_0 = 0$$.  Given that, a one-sided simple/composite test is:
\begin{align}
H_0: F - F_0 =  0, \qquad
H_A: F - F_0 > 0.
\end{align}
Of course, we could just as easily replace the $$>$$ in the alternate with $$<$$.  

The two-sided composite test can be written:
\begin{align}
H_0: F - F_0 = 0, \qquad
H_A: F - F_0 \neq 0,
\end{align}
or equivalently,
\begin{align}
H_0: F = F_0, \qquad
H_A: F \neq F_0.
\end{align}

In other words, the simple null, two-sided composite is equivalent to a test for equality (see below).


Thus, there are essentially three kinds of composite hypotheses:
1. one-sided
2. two-sided
3. not one or two sided (e.g., more complex sets)



### Examples


#### Independent Testing

An independence test is one of the fundamental tests in statistics.   In this case, let $$Z_i = (X_i, Y_i) \sim F_{XY}$$. Now we test:
\begin{align}
H_0: F_{X,Y} = F_{X} F_{Y} \qquad
H_A: F_{X,Y} \neq F_{X} F_{Y}.
\end{align}

In other words, we define $$\mathcal{F}_0$$ as the set of joint distributions on $$(X,Y)$$ such that the joint equals the product of the marginals: $$\mathcal{F}_0 = \{ F_{X,Y} = F_{X}F_{Y} \}$$, and we define $$\mathcal{F}_A$$ as the complement of that set, $$\mathcal{F}_0^c = \mathcal{F} \backslash \mathcal{F}_0 = \mathcal{F}_A$$.  In other words, independence tests are special cases of composite/composite tests.   


#### Two-Sample Testing


Let $$X_i \sim F_1$$, for $$i \in [n]$$ be a random variable, where each $$X_i$$ is sampled independently and identically according to some distribution $$F_1$$.  Realizations of $$X_i$$ are $$x_i \in \mathcal{X}$$.  

Additionally, let $$Y_i \sim F_2$$, for $$i \in [m]$$ be a random variable, where each $$Y_i$$ is sampled independently and identically according to some distribution $$F_2$$.  Realizations of $$Y_i$$ are $$y_i \in \mathcal{Y}$$.  

Given these definitions, all two-sample testing can be written as:

\begin{align}
H_0: F_1 = F_2 \qquad
H_A: F_1 \neq F_2.
\end{align}

This can be written as a composite/composite test.  First, define the mixture distribution $$F = \pi_1 F_1 + \pi_2 F_2$$, where $$\pi_1,\pi_2 \geq 0$$ and  $$\pi_1+\pi_2=1$$. Now, sample $$U_i \sim F$$ for $$n+m$$ times.  To make it exactly equal to the above, set $$\pi_1 = n/(n+m)$$.  Moreover, define $$V_i$$ to be the latent "class label", that is $$V_i=1$$ if $$U_i \sim F_1$$ and $$V_i=2$$ if $$U_i \sim F_2$$.  Now, we can form the independence test:

\begin{align}
H_0: F_{UV} = F_U F_V \qquad
H_A: F_{UV} \neq F_U F_V.
\end{align}

Thus, two-sample tests are special cases of independence tests, which are composite/composite tests.

Moreover, two-sample tests can also be written as simple goodness-of-fit tests, which is readily apparently, as described below.  Thus, simple goodness-of-fit tests are also independence tests.

#### Goodness-of-Fit Testing

The most general kind of a goodness-of-fit test is a composite/composite test:
\begin{align}
H_0: F \in \mathcal{F}_0 \qquad
H_A: F \notin \mathcal{F}_0.
\end{align}
In other words, $$\mathcal{F}_A = \mathcal{F}_0^c = \mathcal{F} \backslash \mathcal{F}_0$$.


The simple/composite test is a special case:
\begin{align}
H_0: F = F_0 \qquad
H_A: F \notin \mathcal{F}_0.
\end{align}



#### K-Sample Tests

More generally, assume there exists $$K$$ different distributions, $$F_1, \ldots, F_K$$, the K-Sample test is:

\begin{align}
H_0: F_1 = F_2 = \cdots = F_K \qquad
H_A: \text{any not equal}.
\end{align}

We can do the same trick as above, defining $$F$$ to be a mixture of $$K$$ distributions, and $$V_i$$ denotes from which component is sample $$i$$. Thus, $$K$$-sample tests are also independence tests.


#### Paired K-Sample Testing


Let $$X_i$$ and $$Y_i$$ be defined as above, except now we sample matched pairs, $$(X_i,Y_i) \sim F_X F_Y$$.  The paired two sample test is still:
\begin{align}
H_0: F = G \qquad
H_A: F \neq G,
\end{align}
but there exists more powerful test statistics that consider the "matchedness". Of course, this also extends to the $$K$$-sample setting.

Note that this is a special case of $$K$$-sample testing, and thus is also an independence test. 

#### Test for Symmetry

Assume we desire to determine whether the distribution of $$X$$ is symmetric about zero.  Define $$F_+$$ as the half of the distribution that is positive, and $$F_-$$ as the half that is negative.  Then, we simply have a typical two-sample test:
\begin{align}
H_0: F_+ = -F_- \qquad
H_A: F_+ \neq -F_-,
\end{align}
which is an independence test.


#### Univariate Examples

Several classic univariate examples illustrate the above three cases.
A classic simple/simple setting is: $$\mathcal{F}$$ is univariate Gaussian,  $$F_0=\mathcal{N}(0,1)$$, and $$F_A=\mathcal{N}(1,1)$$.   A simple/composite generalization of the above is: $$\mathcal{F}$$ is univariate Gaussian,  $$F_0=\mathcal{N}(0,1)$$, and $$\mathcal{F}_A=\mathcal{N}(\mu,1)$$, where $$\mu > 0$$.   A composite/composite generalization of the above is:
For example, $$\mathcal{F}$$ is univariate Gaussian,  $$\mathcal{F}_0=\mathcal{N}(\mu,1)$$ with $$\mu < 0$$, and $$\mathcal{F}_A=\mathcal{N}(\mu,1)$$, where $$\mu \geq 0$$.


#### Counter Examples

The first example given:
\begin{align}
H_0: \theta(F) < 0 \qquad H_A: \theta(F) \geq 0,
\end{align}
is not obviously an independent test.  But maybe it is too.