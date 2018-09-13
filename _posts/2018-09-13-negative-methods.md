---
layout: post
title:  "The Necessity of Negative Results in Methods Papers"
date:   2018-09-13 14:27:57 -0400
tags: misc
author: Joshua Vogelstein
---

I read, write, and review many methods papers.  Based on this, I have some quite opinionated, though I believe well justified views, on what is *required* for a good methods paper to include.  In a later post, I'll provide more details on all the components of a good methods paper.  In this post, I'll simply highlight one thing.

All methods papers spend a great deal of effort convincing the readership that the method is *good*, meaning that it performs well under settings, relative to some existing benchmark methods.  However, the key thing that many methods papers fail to do is:

```
Demonstrate when/why this method performs relatively poorly, as compared to existing methods.
```

This second requirement is crucial because of two related theoretical results.  The first is the [`No Free Lunch Theorem`](https://en.wikipedia.org/wiki/No_free_lunch_theorem), which states:

`
We have dubbed the associated results NFL theorems because they demonstrate that if an algorithm performs well on a certain class of problems then it necessarily pays for that with degraded performance on the set of all remaining problems.
`

[Wolpert, D.H., Macready, W.G. (1997), "No Free Lunch Theorems for Optimization", IEEE Transactions on Evolutionary Computation 1, 67.]

In other words, no method can outperform another method on all possible problems/distributions.  


The other result is the [`Arbitrary Slow Convergence Theorem`](https://link.springer.com/article/10.1007/BF00534199), which states:

  One of the main results of this note is that for every sequence $$f_n$$, and for every positive number sequence an satisfying $$\lim a_n=0$$, there exists an $$f$$ such that $$E(\int \vert f_n(x)−f(x) \vert^p dx)>a_n$$ infinitely often.



In words, if you give me a method to estimate something, i'll give you a distribution such that your estimate will be arbitrarily bad.


Taken together, this means that, in general, no method will dominate any other methods.  The implications of this is that the  goal of a manuscript "cannot" simply be to extoll the greatness of the method.  Rather, it "ought" to be placing it in context.  In particular, to answer: in which settings does it excel (relative to others), and which it does it not?  

If the space of all settings were two-dimensional, than we would want a kind of "[phase diagram](https://en.wikipedia.org/wiki/Phase_diagram)" that partitions the space into regions for which each method is the best.  Such phase diagrams are too difficult to obtain comprehensively typically; therefore, some combination of theoretical and empirical results suffice.  

The reason for this is quite practical.  As a practitioner, I am aware that different methods excel in different settings.  Therefore, my job is to determine which methods are most likely to be most effective in my setting of interest.  The manuscript's job is then to tell me specifically which settings that is the case.  If the manuscript does not indicate when a method performs sub-par, potential users may experience many "false positives", that is, the method may fail in their context.  Ideally when that happens it fails spectacularly, so it is clear to everyone that it has failed.  More likely, it will fail silently, nobody will know that it has failed, but it will provide poor estimates that lead to scientifically invalid/inaccurate claims.  

Given all that, I feel compelled to point out that the space of all functions, or all bounded functions, or all distributions, is quite large.  Therefore, a comprehensive account is typically intractable. Rather, to the extent possible, a manuscript "ought" to explain the general conditions under which the authors expect it to outperform the standard competitors.  Without this, the user will not understand when to use the method.  Perhaps more importantly, without this, the authors of the method might not understand the method particularly well!

Moreover, rather than merely identifying some settings in which the proposed method performs relatively poorly, it is important to explain why that is the case.  While theoretical explanations can be the most concrete and clear, they are often out of scope. Thus, "just so" explanations often suffice.
