---
layout: post
title:  "The Constituents of Decisions"
date:   2018-09-23 14:27:57 -0400
tags: bits
author: Joshua Vogelstein
---

In daily life, we are bombarded with decisions, when to wake up, what to wear, which shoe to tie first, etc.  We all make them all the time.  Moreover, our decisions are often made based on our expectations of the future, with noisy and/or missing data.  For example, what to eat at any time can be dependent on when we expect food to be available again, although that prediction is uncertain.  Therefore, either explicitly or implicitly, we have *rules* governing our behavior, and a set of principles that govern those rules.  

Here, we outline a few basic concepts that I believe essentially *must* be essential components of any system that enables decision making under uncertainty.  To a large degree, this is based on `statistical decision theory`, albeit this treatment is dramatically less formal.  Without further ado, here are the requisite constituents of any decision:

1. **Measurements**: All decisions are based on measurements, and all the measurements must live in some *measurement space*. Often, these measurements are referred to as "data", or "samples".  However, I think labeling them as data can be misleading, because these are in fact physical measurements of *something*.  Regardless of how [accuracy and precise](https://en.wikipedia.org/wiki/Accuracy_and_precision) the measurement apparatus is, all measurements are fundamentally noisy.  Consider, for example, height (the "space" of heights is all positive numbers).  Rulers are highly accurate and precise.  However, the height of an individual changes on the basis of her orientation with respect to the direction of gravity: lie down, and you are a bit taller than when you are standing.  So, measurements of "height" depend on whether you are lying down or standing up.  And if those measurements lack "meta-data" recording your position (and which planet/moon/asteroid you are on, if you are on one), then there is some uncertainty with regard to what is your current height.  In addition to questions of accuracy and precision of the measurement apparatus, there are questions with regard to the [validity](https://en.wikipedia.org/wiki/Validity_(statistics)) of the apparatus, that is, does the measurement truly correspond to the real world concept.  For example, to what extend does an IQ test validly quantify one's intelligence?
 Thus, when describing the measurements, the precision, accuracy, and validity of the measurements ought to be considerations.   Formally, we let $$x_i$$ be the $$i^{th}$$ measurement, and each measurement is in some specified measurement space, $$\mathcal{X}$$.  In the above height example, $$\mathcal{X}= \mathbb{R}_{\ge 0}$$. Let $$\{x_i\}$$ denote the set of all observed measurements.


2. **Actions**: If a decision must be made, the answer is one of several possible *actions*.  Technically, these actions need not be physical body actions, they could be believes as well.  For example, I can decide that I love something, or everything.  No physical action is required. Other actions include estimates, such as, the mean height of people in the world, or conclusions, such as the mean height is greater than zero.  Formally, a possible action $$a$$ is an element of an action space, $$\mathcal{A}$$.

3. **Decision Rule**:  Something, or someone, must take as input the measurements, and output an action.  A human can do this, or a mechanical devise, or some combination of the two, e.g., a human operating a computer.  Formally, a decision rule, $$\delta_n : \mathcal{X}_n \to \mathcal{A}$$.

4. **Loss function**: The decision rule must somehow *choose* which action to take, on the basis of the measurements.  To do so, it must operate, either implicitly or explicitly, according to a loss function.  For example, that loss function could be to minimize squared error, or maximize historical returns, without exceeding a certain variance, etc. Regardless of its form, it quantifies the *loss* experienced by the decision rule if were to decide on  any specific action, given the input measurements. Formally, loss is a function, $$\ell : \mathcal{A} \to \mathbb{R}$$.


And that is all.  No other constituent parts are required to make decisions. Moreover, certain theoretical claims are available even under this very simple setting.  For example, one can prove that a given decision rule will converge to a fixed point, regardless of the input measurements, for a given loss.   Other things are required, however, for stronger theoretical claims, which will be the subject of a future blog post.



<!-- 3. **Estimator** (or **learner**):  Something, or someone, must take as input the measurements, and output an action.  A human can do this, or a mechanical devise, or some combination of the two, e.g., a human operating a computer.  Note, however, that mechanical devises, on their own (at least for now), cannot estimate/learn without human intervention. -->
