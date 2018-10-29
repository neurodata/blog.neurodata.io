---
layout: post
title: What is Statistics For?
description: ""
modified: 2016-12-18
category: misc
author: Joshua Vogelstein
tags: [publicity, collaboration]
imagefeature: to_the_cloud.jpg
comments: true
share: true
featured: true
---

Statistics can serve many purposes.
As humans, we tend to like partitioning the world into bins, and assigning each bin some semantic label.
Though we sometimes forget that the boundaries are typically not that clear,
and that there exist cases that are ambiguous or on the "wrong" side of the boundary,
the labels are still useful by reducing variance, even if they are increasing bias.
So, my implicit bias/variance trade-off for statistics leads me to partition statistics into 3 different roles:

1. **Descriptive**: Describing the data at hand, its moments, its anomalies, etc. All descriptive statistics are functions that operate on the dataset, and output a scalar, a vector, or some other object.  Crucially, descriptive statistics make no assumptions about the data, they merely describe it. They cannot be right or wrong, though they can be misleading.
2. **Predictive**: Predicting what would happen in some hypothetical other dataset.  The crucial difference between predictive and descriptive statistics is that predictive statistics *must* make assumptions, and these assumptions invariably simplify the true data generation process, and therefore are incomplete/imperfect in various ways. The quality/accuracy of the predictions will thus hedge on the quality/accuracy of the underlying assumptions.  For this reason, assessing the predictive accuracy correctly benefits from *understanding the assumptions* in the predictive process "soup to nuts".  That is, understanding more about the assumptions in each step of the pipeline, starting with experimental design, through data collection and analysis.  Scientific results are essentially only interesting insofar as they are predictions: What happened on any particular dataset is anecdotal, not scientific.  A prediction can be right or wrong, or misleading (right/wrong for some unexplained reason).
3.  **Manipulative**: Manipulating the world includes experimental design and control, as key examples.  In its manipulative capacity, the quality of the manipulations, just like the quality of predictions, depends on the assumptions.  Much like "an ounce of prevention is worth a pound of cure", a bit of manipulative statistics can be worth more than all the possible post-data-collection descriptions & predictions anyone can make. Manipulations can have varying degrees of utility, and when they are using predictions, the predictions can be right or wrong.


Science gets into trouble when it interprets descriptive statistics as predictive, or the scientists (or journalists) misunderstand certain assumptions that underly the procedures, and therefore, the interpretation/accuracy/veracity of the predictions.
