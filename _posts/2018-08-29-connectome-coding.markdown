---
layout: post
title:  "Connectome Coding"
date:   2018-08-29 14:27:57 -0400
tags: [brains, bits]
author: Joshua Vogelstein
---

The following are notes based first on an invited talk I gave at [Baylor](http://dx.doi.org/10.6084/m9.figshare.1140321), and then a tutorial I gave at [SfN](https://neurodata.io/talks/sfn17.html).  More recently, I was asked to write an article for [Current Opinion in Neurobology](https://www.sciencedirect.com/journal/current-opinion-in-neurobiology), which will be based largely on this blog post, which is content that flowed most recently from conversations with [Brett Mensh](http://optimizescience.com/) and [Carey E. Priebe](https://www.ams.jhu.edu/~priebe/).

---------------


# What is connectome coding?

To define connectome coding, we define both `code` and `connectome`.  Let's start with `code`:


`
A code is a system of (potentially stochastic) rules that translate from one representation of information into another.  
`

In the language of statistics, a code is a conditional distribution, of a pair of random variables, $$X$$ and $$Y$$, $$P[Y \vert X]$$. This conditional distribution tells us the probability that given random variable $X$ takes some value from it set of possible values $$x \in \mathcal{X}$$,  that $$Y$$ takes any of its possible values, $$y \in \mathcal{Y}$$.  In other words, $$P[Y \vert X]$$ is the probabilistic rule converting from $$x$$ to $$y$$.



OK, now that `code` is hopefully clear, what is `connectome`?

```A connectome is a network of the brain, at a particular time, for a particular spatiotemporal scale, potentially including vertex attributes such as names, locations, and labels in a hierarchical ontology, as well as edge attributes such as weights and confidences.  Both vertex and edge attributes can have morphological properties characterizing their  three-dimensional (3D) shapes.  Note that each individual vertex and edge is  contiguous in space.
```

OK, now we have `code` and `connectome` definitions. So a connectome code is a conditional distribution, where either $$X$$ or $$Y$$ corresponds to the random variable whose realizations are connectomes.  But what is the other random variable representing?

To explain that, we take a step back, and provide our conceptual model of brains, bodies, and worlds (see below image). Worlds contain bodies which contain brains. And brains are composed both both structure (which we think of as basically "static") and activity (which we think of as basically "dynamic").  The brain's job is to direct the body's behavior so that the organism wins the evolutionary game in its particular niche of the world (its environment), and propagates its genes to the next generation.  The structure of the brain, its **connectome**, is determined jointly by developmental programs (encoded in the genome), and activity dependent plasticity (resulting from ongoing brain activity, which in turn is dependent on the body and world).

![](../../../_site/assets/brain-body-world)

![]("/assets/brain-body-world")

![](https://neurodata.io/talks/images/brain-body-world.png)

<!-- <img src="brain-body-world" STYLE="HEIGHT:95px;"/> -->

Let's model each of those things as random variables: $$E$$ is the environment, $$B$$ is behavior, $$A$$ is activity, $$C$$ is connectome, and $$D$$ is development, as specified by the genome. Based on this, we can now define connectome coding as a conditional distribution, where either something is conditioned on connectomes, or connectomes are conditioned on something else.

First, consider $$P[C \vert D]$$, which specifies the probability of an individual having a specific connectome, conditioned on her genome.  In other words, in this model, the genome must *encode* the probabilistic rules of connectivity, at some resolution, to ensure that the connectome can function sufficiently well in the expected environmental "niche" that the organism is in.  Second, consider $$P[A,B,E \vert C]$$, which specifies the probability  of the world state, a body position, and its brain's activity conditioned on a particular connectome.  One can also "marginalize" out $$E$$, $$B$$, and/or $$A$$ to get $$P[A \vert C]$$, or $$P[B \vert C]$$, or $$P[A,B \vert C]$$, etc.  Once one has both the above conditional distributions, it is natural to inquire about the full joint, $$P[A, B, C, D, E]$$.  

Although one can write all of the above conditioned regardless of the causal graph, there is an implicit causal graph.  Specifically, $$D \Leftarrow C \Leftrightarrow A \Leftrightarrow B \Leftrightarrow E$$.  What are the implications of this causal dependence structure?  For the genome to encode the probabilistic rules of behavior, to facilitate the organism winning the evolutionary game, it **must** go through the connectome.  A natural question therefore is:

`
How can a genome encode rules governing behavior?
`

Since behavior is ongoing, dynamic, and responsive to the environment, and the somatic genome is static, it must essentially encode a blueprint that *guides* the construction of a vessel whose physical properties are such that they encourage "high value" behaviors.  That vessel is the connectome.  In other words, **the connectome is the mechanism by which the genome can encode its preferred behaviors, that, when combined with the body, and physics, yields the desired behaviors with sufficiently high probability to help the organism win the evolutionary game its niche imposes on it.**    



This view of connectomes, and connectome coding, is, to our knowledge, essentially novel.  Whether this view is useful remains to be seen, and will be born out if/when people take the view seriously, and try to discover meaningful insights about the brain, how it works, and how it fails.
