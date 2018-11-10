---
layout: post
title:  "The Varieties of Hypothesis Tests"
date:   2018-09-29 14:27:57 -0400
tags: bits
author: Joshua Vogelstein
---

Hypothesis testing is a procedure for evaluating the likelihood that a given dataset corresponds to a particular "null" model.   Formally, all hypothesis testing scenarios can be described as follows.


Let $$X_i \sim F$$, for $$i \in [n]=\{1,\ldots,n\}$$ be a random variable, where each $$X_i$$ is sampled independently and identically according to some distribution $$F$$.  Realizations of $$X_i$$ are $$x_i \in \mathcal{X}$$.  We further assume that $$F \in \mathcal{F}$$, that is, $$F$$ is a distribution that lives in a model $$\mathcal{F} = \{F : \mathcal{F}\}$$.  Moreover, we partition $$\mathcal{F}$$ into two complementary sets, $$\mathcal{F}_0$$ and $$\mathcal{F}_A$$, such that $$\mathcal{F}_0 \cup \mathcal{F}_A = \mathcal{F}$$ and $$\mathcal{F}_0 \cap \mathcal{F}_A = \emptyset$$.  Given these definitions, all hypothesis tests can be written as:

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

Note that composite tests (those where the null or alternate is composite) can be both one-sided or two-sided.  In particular, the simple null hypothesis can be restated: $$H_0: F-F_0 = 0$$.  Given that, a one-sided simple/composite test is:
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
1. one-sided,
2. two-sided, or 
3. neither (e.g., the alternative is a more complex set).



### Examples


#### Independence Testing

An independence test is one of the fundamental tests in statistics.   In this case, let $$Z_i = (X_i, Y_i) \sim F_{XY}$$. Now we test:
\begin{align}
H_0: F_{X,Y} = F_{X} F_{Y} \qquad
H_A: F_{X,Y} \neq F_{X} F_{Y}.
\end{align}

In other words, we define $$\mathcal{F}_0$$ as the set of joint distributions on $$(X,Y)$$ such that the joint equals the product of the marginals: $$\mathcal{F}_0 = \{ F_{X,Y} = F_{X}F_{Y} \}$$, and we define $$\mathcal{F}_A$$ as the complement of that set, $$\mathcal{F}_0^c = \mathcal{F} \backslash \mathcal{F}_0 = \mathcal{F}_A$$.  Independence tests are special cases of C/C tests.   


#### Two-Sample Testing


Let $$X_i \sim F_1$$, for $$i \in [n]$$ be a random variable, where each $$X_i$$ is sampled independently and identically according to some distribution $$F_1$$.  Realizations of $$X_i$$ are $$x_i \in \mathcal{X}$$.  

Additionally, let $$Y_i \sim F_2$$, for $$i \in [m]$$ be a random variable, where each $$Y_i$$ is sampled independently and identically according to some distribution $$F_2$$.  Realizations of $$Y_i$$ are $$y_i \in \mathcal{Y}$$.  

Given these definitions, all two-sample testing can be written as:

\begin{align}
H_0: F_1 = F_2 \qquad
H_A: F_1 \neq F_2.
\end{align}

This can be written as an independence test.  First, define the mixture distribution $$F = \pi_1 F_1 + \pi_2 F_2$$, where $$\pi_1,\pi_2 \geq 0$$ and  $$\pi_1+\pi_2=1$$. Now, sample $$U_i \sim F$$ for $$n+m$$ times.  To make it exactly equal to the above, set $$\pi_1 = n/(n+m)$$.  Moreover, define $$V_i$$ to be the latent "class label", that is $$V_i=1$$ if $$U_i \sim F_1$$ and $$V_i=2$$ if $$U_i \sim F_2$$.  Now, we can form the independence test:

\begin{align}
H_0: F_{UV} = F_U F_V \qquad
H_A: F_{UV} \neq F_U F_V.
\end{align}

Moreover, two-sample tests can also be written as simple goodness-of-fit tests, which is readily apparent, as described below.  Thus, simple goodness-of-fit tests are also independence tests.


#### Goodness-of-Fit Testing

The most general kind of a goodness-of-fit test is a C/C test:
\begin{align}
H_0: F \in \mathcal{F}_0 \qquad
H_A: F \notin \mathcal{F}_0.
\end{align}
In other words, $$\mathcal{F}_A = \mathcal{F}_0^c = \mathcal{F} \backslash \mathcal{F}_0$$.


The S/C goodness-of-fit test is a special case:
\begin{align}
H_0: F = F_0 \qquad
H_A: F \neq F_0.
\end{align}

This special case is clearly an instance of a two-sample test; the only difference is that the second distribution is not estimated from the data, but rather, is provided by the null. 

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


#### Multinomial Test

Assume $$X \sim $$Multinomial$$(p_1, p_2, p_3; n)$$, and let:
\begin{align}
H_0: p_1 = p_2 = p_3 \qquad
H_A: \text{not all equal}.
\end{align}

This is again a $$K$$ sample test, which is an independence test.

Considering a slightly different case:
\begin{align}
H_0: p_1 = p_2 \qquad
H_A: p_1 \neq n_2.
\end{align}
This is a slight generalization of the above, but can still be written as a $$K$$ sample test, and is therefore an independence test.


#### One Sided Test

Assume $$X \sim \mathcal{N}(\mu,1)$$, and consider the following test:
\begin{align}
H_0: \mu = 0 \qquad
H_A: \mu \neq 0.
\end{align}

This is a two-sample test, and therefore, an independence test.  A slightly more complicated variant is:
\begin{align}
H_0: \mu < 0 \qquad
H_A: \mu \geq 0.
\end{align}

Viewing this as an independence test is a bit more complicated.  In particular, if we set it up as the above two-sample test, and we reject, it could be because $$\mu < 0$$ or because $$\mu > 0$$.  However, in practice, it is difficult to address.  Letting our test statistic be $$\bar{x}= \frac{1}{n} \sum_i x_i$$, we consider four scenarios:

1. If $$\bar{x} < 0$$, and we reject, then we know that $$\bar{x}$$ is significantly below $$0$$, and therefore, we should *not* reject the real null.  
2. If $$\bar{x} < 0$$ and we fail to reject, then we have failed to reject our original hypothesis, and we are ok.
3. If $$\bar{x} > 0$$, and we reject, meaning that $$\bar{x}$$ is significantly above $$0$$, and therefore we are safe to reject the null.
4. If $$\bar{x} > 0$$, and we fail to reject, that means $$\bar{x}$$ is not significantly bigger than zero, but we cannot reject the original null.

Thus, we can use the test for whether $$\mu=0$$, probably at a fairly severe reduction in power, but nonetheless, maintain a valid test. 