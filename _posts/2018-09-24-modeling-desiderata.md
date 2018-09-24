---
layout: post
title:  "Deciding Stuff Under Uncertainty"
date:   2018-09-23 14:27:57 -0400
tags: misc
author: Joshua Vogelstein
---


1. **Sufficiency**: to answer them.  This means that the framework must be able to represent graphs with complex vertex and edge attributes.  validity of measurements.

2. **Quantify Uncertainty**:  
Second, the connectomes on which the framework will operate are fundamentally noisy, the measurements are noisy, and probably the actual connection probabilities in the brain are stochastic.  For example, even a identical twins, or clones, are unlikely to have identical connectomes at all scales.
This means that the modeling framework must incorporate and \emph{quantify uncertainty}.

3. **Flexibility**:
Third, the latent geometric and topological structures that guide the development of connectomes, and that guide the activity given connectomes, could be arbitrarily complex.  The modeling framework should be able to discover such latent properties.

4. **Consistency**:
Fourth, that the modeling framework incorporates uncertainty implies the existence of parameters with unknown values, that we desire to estimate from the observed data.
Thus, the modeling framework must be able to provide theoretical guarantees about the ``validity'' and/or ``correctness'' of the parameter and uncertainty estimates, given sufficient data, under the assumed model. In other words, if one desires to estimate the average connectome from a population, and the estimator of the average may or may not converge to the truth, why would one trust that estimate~\cite{Tang2016-conn}.
Estimators with this property are called {consistent}'' in the statistics literature~\cite{Bickel2000-kb}.

5. **Robustness** and **Stability**:
Fifth, standard consistent results imply that the estimators converge under certain model assumptions.  However, "all models are wrong", which means that we also desire that our estimators perform well despite model uncertainties; in other words, that our estimators are \emph{robust}.

6. **Statistical Efficiency**:


7. **Computational Efficiency and Scalability**:
Sixth, using this model to make inferences must be computationally tractable, or better yet, \emph{computationally efficient} (for example, polynomial computing time).  Graph theoretic problems are notorious computationally difficult~\cite{Lyzinski2016-hb}.  Thus, for many questions, either analytic or numeric approximations are necessary to obtain polynomial (rather than exponential) time algorithms.  
We desire that despite those approximations, estimates preserve their consistency properties.  

8. **Usability**:
