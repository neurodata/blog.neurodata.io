---
layout: post
title:  "10 Simple Rules to Developing a New Method"
tags:  [10,bits]
author: Joshua Vogelstein
---



So you want to develop a new method.  I recommend you do the following:


0. **Find something about the world that you'd like to be better**
My recommendation is to read [how to choose a project](https://bitsandbrains.io/2018/08/31/sig-and-feas.html), and find the project that maximizes feasibility and significance for you, given you intrinsic motivation.  This is the hardest part, but once you have done this, you'll hopefully have both purpose and direction.

1. **Write down the mathematical problem you are trying to solve that will improve the world for the above described project**
Using as formal notation as possible, write down the goal of your method.  Is it a classification problem? Are there any particular constraints?  Which of [these things](https://bitsandbrains.io/2018/09/24/modeling-desiderata.html) do you particularly care about, and how much, and what constraints do you have.  I particularly like the example provided in my [signal subgraph paper](https://dl.acm.org/citation.cfm?id=2498823).

1. **Identify Reference Methods** Identify the current state-of-the-art (SoA) methods for solving this problem.  Make a list of references (up to five articles) describing SoA, and highlight those for which you can identify reference implementations.  For python users, compare to at least  one relevant algorithm in [sklearn](https://scikit-learn.org/stable/), and probably a few others (sklearn only includes algorithms that are at least three years old, so it never has the most up-to-date algorithms). For R users, search through the [CRAN Task Views](https://cran.r-project.org/web/views/).

1. **Identify Benchmark Settings**
The previous SoA must have run their code on some datasets, including both simulated and real.  Identify those settings.  We will be comparing our algorithm's performance on those settings, so as to not be cherry-picking settings.  Also consider a few (like one or two) very simple real datasets, such as [sklearn's toy datasets](https://scikit-learn.org/stable/datasets/index.html#toy-datasets).

1. **Identify Metrics**
The best metrics will depend on your goals.  For example, in classification, held-out classification error might be the best metric, but other metrics can also be useful, for example, see the metrics we used in our [sporf paper](https://arxiv.org/abs/1506.03410), which include a normalized effect size variant of Cohen's kappa.

2. **Understand Geometry**
Describe in detail (as formally as you can) the simplest parametric model that you will be using to evaluate this algorithm. This model should have the property that you can change a one-dimensional parameter to make vary the performance of your algorithm from better thant the current SoA to worse than the current SoA. For example, e.g., k-means will work better than GMM when two clusters are all spherically symmetric Gaussians and each cluster is equally likely, but will work worse than GMM when one cluster is much more likely than the other. Therefore, the probability of a cluster is the one-dimensional parameter that illustrates the phase transition in for the algorithms.  If you can't figure out a single simple illustration for this, come up with two different simple settings: one for which you expect your new algorithm to outperform the SoA, and one for which you expect your new algorithm to under-perform the SoA. In this case, vary some property of both settings (for example, number of dimensions, or variance), to demonstrate the robustness of the result across this dimension. To the extent possible, use previously proposed settings, such as the ones in sklearn's [clustering](https://scikit-learn.org/stable/modules/clustering.html) or [sample generators](https://scikit-learn.org/stable/modules/classes.html#module-sklearn.datasets); we have also proposed several in our papers, such as [mgc](https://elifesciences.org/articles/41690), [sporf](https://arxiv.org/abs/1506.03410), and [geodesic forests](https://arxiv.org/abs/1907.02844).


1. **Simulate**
Write code to simulate those scenarios, and look at the results.  Confirm that your simulations are in fact simulating what the equations describing the simulations meant to describe. 

1. **Run Previous SoA**
   1. Make a Jupyter notebook running previous SoA on the simulations and data from their paper.  Make sure your results at least approximately match their reported results (like, within 1%); ideally your results are identical to the published results, but that is not typical.  This is especially important if you are re-implementing the previous SoA, rather than simply using their results.  
   2. Make a Jupyter notebook on any additional simulation settings.  
   3. PR the part of this Jupyter notebook that includes an sklearn algorithm.


2. **Pseudocode, Code, and Test**
   1. Write pseudocode (as formally as you can) for your algorithm.  I particularly like the text explanation pseudocode that we wrote for our [mgc paper](https://elifesciences.org/articles/41690).
   2. Write the code for your algorithm.  If you are in Python, to the extent possible, follow the [sklearn API](https://scikit-learn.org/stable/developers/contributing.html#apis-of-scikit-learn-objects).
   3. Test your code on very simple experimental settings.  Settings which should result in an obvious result.  I recommend the following three tests:
       1. A setting in which it is so easy that for sure any reasonable algorithm will get the answer perfect.  
       2. A setting which is impossible for your algorithm to get right.  
       3. A reasonable setting, in which as sample size increases, accuracy should improve.
   If your implementation works as expected in all of these settings, proceed.  Otherwise, iterate.

3. **Evaluate Algorithm on Simulations**
Make a Jupyter notebook evaluating all the  algorithms on the simulations. For each simulation setting:

   1. Generate 10x random samples of the data
   2. Run all relevant algorithms.
   3. Compare performance (using the above established metrics) on each run of the simulation.  That is, do not compare the average, but rather, make 10 comparisons.  Comparing each run is more powerful and informative.
   4. Plot all 10x comparisons for each algorithm compared to yours.

3. **Evaluate Algorithm on Real Data**
Make a Jupyter notebook evaluating all the  algorithms on the simulations. For each real data setting:

   1. Run 5-fold or 10-fold cross-validation. When appropriate, use stratified cross-validation.  Do cross-validation such that the data are divided into k (approximately) equal sizes subsets of data.  Train on the k-1 subsets and test on the remaining subset, so that each sample is used for testing exactly once.   
   2. Run all relevant algorithms.
   3. Compare performance (using the above established metrics) on each fold.  That is, do not compare the average, but rather, make k comparisons.  Comparing each run is more powerful and informative.
   4. Plot all 10x comparisons for each algorithm compared to yours.




*************************

If you follow the above plan, you will carefully demonstrated the value of your new algorithm in an unambiguous fashion. 