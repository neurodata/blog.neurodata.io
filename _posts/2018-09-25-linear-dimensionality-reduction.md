---
layout: post
title:  "10 Methods for Linear Dimensionality Reduction"
date:   2018-09-25 14:27:57 -0400
tags: [bits, 10]
author: Joshua Vogelstein
---

Colleagues and trainees have asked for a basic summary of different linear dimensionality reduction methods.  Here is my take on them.

1. PCA - finds the directions of maximal variance in your data matrix.  It **actually solves for the right answer**, that is, finds the true optimal dimensions. they are optimal in the sense that they are the best dimensions for finding a low-dimensional representation that minimizes squared error loss.  This means it cannot be beat by fancy things like manifold learning, etc., **for squared error loss**.  In practice, squared error loss is typically not what we really want to optimize.

2. ICA - As it turns out, PCA finds directions that are orthogonal (perpendicular to one another).  If one simply relaxes this constraint, one obtains ICA.  Unlike PCA however, **there is no guarantee that the algorithm finds the optimal answer**.  The objective function is non-convex, so the initialization matters.  I am not familiar with any theory that states the answer any particular approach has guaranteed performance, meaning, one can never say with high probability the answer is very good (when running ICA).  It is commonly used for blind signal separation in some disciplines.  Often initialized by PCA. There are many extensions/generalizations of ICA.

3. NMF - related to ICA in certain ways, in that it changes the constraints of PCA. For this, it helps me to think of PCA as a matrix factorization problem, where there are loading vectors and principal components.  The PC's are constrained to be orthonormal, meaning orthogonal and each one sums to one.  In NMF, **one or both of the matrices are constrained to be non-negative**.  This is particularly useful when you have domain knowledge that the "truth" is non-negative, such as images.  However, in practice, simply running PCA and then truncating things below zero to equal zero often works as well with much less hassle.

4. LDA - Here, rather than merely a "data matrix", we also have a target variable that is categorical (eg, binary).  Where as PCA tries to find the directions that maximize the variance, **LDA finds the 1 dimension that maximizes the "separability" of the two classes**, under a gaussian assumption.  It is consistent under the gaussian assumption, meaning if you have enough data, it will eventually achieve the optimal result.

5. Linear regression - Same as LDA, but her the target variable is continuous, rather than categorical. **So, linear regression finds the 1 dimension that "is closest" to the target variable**. As it turns out, in a very real sense, linear regression is a strict generalization of LDA, meaning that if one runs linear regression on a two-class classification problem, one will recover the same vector that LDA would provide.  Like LDA, it is optimal under a gaussian assumption if you have enough data.

6. CCA - Is a generalization of linear regression and LDA, which applies when you have multiple target variables (eg, height and weight).  CCA finds the dimensions of both the "data matrix" and the "target matrix" that j**ointly maximize their covariance**.  if the target matrix is one-dimensional, it reduces to linear regression. if it is one-dimensional and categorical, it reduces to LDA.  Again, it achieves optimality under linear gaussian assumptions with enough data.

7. PLS - Like CCA, but rather than maximizing covariance, it **maximizes correlation** between the learned dimensions.  Often this works better than CCA and other stuff.  The geometry and theory underlying PLS is much less clear, however, and efficient implementations are less readily available.

8. JIVE - Also like CCA, in the sense that there are multiple modalities, but now there are also multiple subjects, and each subject has matrix valued data (and each matrix is the same size/shape/features).  JIVE explicitly tries to model the variance that is **shared across individuals**, and separate it out from the subject specific signal, which is also separated from subject specific noise. It does so by imposing several constraints, specifically that features are orthogonal to one another.

9. LOL - We made this one up; the arxiv version is [here](https://arxiv.org/abs/1709.01233).  It is designed to find a low-dimensional representation  **when dimensionality is much larger than sample size**.  We proved that, under gaussian assumptions, it works better than PCA and other linear methods for subsequent classification.

10. Random Projections - These have support from an elegant theory, the [Johnson–Lindenstrauss lemma](https://en.wikipedia.org/wiki/Johnson%E2%80%93Lindenstrauss_lemma), which states that "random" projections, can achieve low reconstruction error with high-probability.  There are many possible ways to generate these random projections, my favorite way is [very sparse random projections](https://dl.acm.org/citation.cfm?id=1150436), which simply requires a few non-zero numbers, and the rest can be +1 or -1.  We use this result to accelerate LOL.

Others have written/compared all the various linear methods in greater detail, one example is [here](https://stat.columbia.edu/~cunningham/pdf/CunninghamJMLR2015.pdf), which addresses many of the methods i discussed above, as well as some others (but misses a PLS and JIVE).
