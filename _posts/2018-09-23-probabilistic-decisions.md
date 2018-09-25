---
layout: post
title:  "Deciding Stuff Under Uncertainty"
date:   2018-09-23 14:27:57 -0400
tags: bits
author: Joshua Vogelstein
---

In a [previous post](https://blog.neurodata.io/2018/09/23/deciding-stuff.html), we enumerated the four necessary constituents for deciding anything: (1) measurements, (2) potential actions, (3) a decision rule, and (4) a loss function.  Many great things have come from this stylized setting, including essentially everything in the fields of "pattern recognition" and "data mining". One can often obtain stronger theoretical results, and better empirical performance, by adopting additional assumptions/structure to the decision process. Here are three additional constituents that are essentially required when incorporating uncertainty.

1. **Probabilistic Generative Model**: This is a set of probability distributions under consideration.  For example, "Gaussian" can be a probablistic generative model (or "model", for short), where all Gaussian distributions, each characterized by a particular mean and variance, are elements of the model.  Note that if there are multiple measurements being used to make a decision, some assumptions are required to link those measurements.  The simplest, and probably most commonly used assumption, is that each measurement is sampled independently and identically from a true but unknown distribution in the model. Formally, $$\mathcal{M} = \{\theta : F_\theta \in \mathcal{M} \}$$.

2. **Estimator**: To quote wikipedia, who was quoting Tukey, "an *estimator*   is a rule for calculating an estimate of a given quantity based on observed data: thus the rule (the estimator), the quantity of interest (the estimand) and its result (the estimate) are distinguished." In this context, estimators  estimate a decision rule, which chooses an action.   For example, in linear discriminant analysis, the estimator *learns* the decision boundary, and the estimate *is* the decision boundary.  Formally, an estimator is a function, $$f_n: \mathcal{X}_n \to \Delta$$, where $$\Delta = \{\delta\}$$ is the set of admissible decision rules.

3. **Risk Functional**: Under uncertainty, a given decision rule will incur losses probabilistically depending on the particular realized measurements.  Therefore, simply minimizing loss on the observed measurements may not be desirable, and in particular, may result in over-fitting.  It is therefore more desirable to choose/learn a decision rule that minimizes some functional of the distribution of loss induced by the true but unknown distribution.  For example, one may desire a decision rule that minimizes the expected loss.  In other contexts, one may instead desire a decision rule that minimizes the expect loss subject to a constraint on the size of the expected variance.  This comes up, for example, in financial portfolio optimization.


With these three additional constituents, one can begin constructing estimators that have desirable properties, as will be described in the [next post](https://blog.neurodata.io/2018/09/23/modeling-desiderata.html).



<!-- 3. **Estimator** (or **learner**):  Something, or someone, must take as input the measurements, and output an action.  A human can do this, or a mechanical devise, or some combination of the two, e.g., a human operating a computer.  Note, however, that mechanical devises, on their own (at least for now), cannot estimate/learn without human intervention. -->
