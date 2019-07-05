---
layout: post
title:  "Bilateral Homology"
date:   2019-02-10 14:27:57 -0400
tags:  [brains, bits]
author: Joshua Vogelstein
---

Homology, means having the same or similar relation, relative position, or structure.
In biology, [homology](https://en.wikipedia.org/wiki/Homology_(biology)) usually refers to comparison across taxa, like human vs non-human primate. 
Two biological structures are homologous in different taxa if they are derived from a common ancestor, such as feet and flippers.

Within an individual, people speak of [bilateral symmetry](https://en.wikipedia.org/wiki/Symmetry_in_biology#Bilateral_symmetry), 
which means there is an approximate reflection symmetry about some body axis. 
For example, the human cortex is bilaterally symmetric. This is despite the fact that the left side has regions of the brain that are not present in the right side.  
In other words, if one were to quantify the degree of differences between the two sides, bilateral symmetry only requires that the difference between the two sides is less than some threshold.  Where one puts the threshold is a subjective matter.  

Bilateral homology is a relatively new concept.  For now, we say that two biological structures are bilaterally homologous if, under "normal" environmental conditions, the degree of bilateral symmetric is $c$, 
and under certain perturbations of the conditions, the degree of bilateral symmetry is $$c'$$, and $$c' > c$$. Which means that, by definition, any "normal" connectome cannot exhibit bilateral homology.

To be a bit more concrete, for a particular individual, we observe $n$ points from one side, $$x_1,\ldots, x_n$$, and $m$ points from the other side, $y_1,\ldots, y_m$. 
Assume that each observation is sampled independently from the others, and that those from the first side are sampled from some true but unknown distribution $F$, and those from the other side are sampled from some  true but unknown distribution $G$.  We can then posit a formal hypothesis test:

$$H0: F = G, \qquad  HA: F \neq G$$

Implementing this test requires choosing a test statistic 

$$t=t( x_1,...,x_n, y_1,..., y_m) \in \mathcal{Real},$$

and we reject bilateral homology if and only if the observed $t$ is more extreme than $(1 - \alpha)\%$ of the time under the null.

This test, like all other tests, requires a distribution of the test statistic $t$ under the null. One way to proceed would be to acquire S "typical" individuals, and compute $t$ for each of them. Then, given 1 individual that experienced an experimental perturbation, we could accurately ascertain how extreme this individuals test statistic is relative to the "typical" ones.  This approach, of course, is sensitive to both the choose of test statistic and model: $F, G \in \mathcal{F}$.  Nonetheless, reasonable choices for both are available in many situations.

On the other hand, in the absence of S typical individuals, how might one proceed?  One could sample S times from an estimated null.  This would depend *strongly* on $\mathcal{F}$, but is still possible.


Now, assume we observe only a single typical individual. The question we are interested in asking is: are the left and the right "more different than one would expect by chance?".  Since we've only observed 1 individual, how might we go about estimating the null? One option would be to fit a series of increasingly complex models to the one side, $\mathcal{F}_1, \mathcal{F}_2, \ldots$, and ascertain their model fit the other side. Then, do the same training models on the right, and ascertaining them on the left. Assuming for simplicity that both experiments revealed that the same model was the best fit across sides, we can operate under the assumption that this is a reasonable model.  Now, we can proceed as proposed above: using this selected model, estimate the null distribution by sampling, which provides a p-value.   