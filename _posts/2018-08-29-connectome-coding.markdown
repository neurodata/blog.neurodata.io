---
layout: post
title:  "Connectome Coding"
date:   2018-08-29 14:27:57 -0400
categories: [brains, bits]
author: Joshua Vogelstein
---

The following is a draft/summary of an article we are writing.  We'd love any feedback that you have, especially critical.



`what is connectome coding?`

Well, to define connectome coding, we define both `code` and `connectome`.  Let's start with `code`:


### A code is a system of (potentially stochastic) rules that translate from one representation of information into another.  

In the language of statistics, a code is a conditional distribution, $$P[Y \vert X]$$.  More specifically, let $$x$$ be an element of some set $$\mathcal{X}$$, and let $$X$$ be a random variable whose realizations are $$\{x : x \in \mathcal{X}\}$$.  For example, $$X$$ could be a Bernoulli random variable, so $$x \in \{0,1\} = \mathcal{X}$$.  Similarly, $$y$$ is an element of a set $$\mathcal{Y}$$ and $$Y$$ is a random variable whose realizations are $$\{y : y \in \mathcal{Y}\}$$.  Note that, in general, $$\mathcal{X}$$ and $$\mathcal{Y}$$ need not be the same sets.  For example, $$\mathcal{Y}$$ could be the real number line, or the set of all circles, or trees, or dolls, etc.  

OK, now that `code` is hopefully clear, what is `connectome`?

### A connectome is a network of the brain, at a particular time, for a particular spatiotemporal scale, potentially including vertex attributes such as names, locations, and labels in a hierarchical ontology, as well as edge attributes such as weights and confidences.  Both vertex and edge attributes can have morphological properties characterizing their  three-dimensional (3D) shapes.  Note that each vertex and edge is a contiguous  3D object.

OK, now we have `code` and `connectome` definitions. So a connectome code is a conditional distribution, where either $$X$$ or $$Y$$ corresponds to the random variable whose realizations are connectomes.  But what is the other random variable representing?

To explain that, we take a step back, and provide our general philosophy on brains, bodies, and worlds.
Worlds contain bodies which contain brains.
And brains are composed both both structure (which we think of as basically "static") and activity (which we think of as basically "dynamic").  The brain's job is to direct the body's behavior so that the organism wins the evolutionary game in its particular niche of the world (its environment), and propagates its genes to the next generation.  

Let's model each of those things as random variables: $$E$$ is the environment, $$B$$ is behavior, $$A$$ is activity, $$C$$ is connectome, and $$D$$ is development, as specified by the genome. Based on this, we can now define connectome coding as a conditional distribution, where either something is conditioned on connectomes, or connectomes are conditioned on something else.

First, consider $$P[C \vert D]$$, which specifies the probability of an individual having a specific connectome, conditioned on her genome.  In other words, in this model, the genome must `encode` the probabilistic rules of connectivity, at some resolution, to ensure that the connectome can function sufficiently well in the expected environmental "niche" that the organism is in.  Second, consider $$P[A,B,E \vert C]$$, which specifies the probability  of the world state, a body position, and its brain's activity conditioned on a particular connectome.  One can also "marginalize" out $$W$$, $$B$$, and/or $$A$$ to get $$P[A \vert C]$$, or $$P[B \vert C]$$, or $$P[A,B \vert C]$$, etc.  

Once one has both conditional distributions, it is natural to inquire about the full joint, $$P[A, B, C, D, E]$$.  However,  although one can write all of the above conditioned regardless of the causal graph, there is an implicit causal graph.  Specifically, $$E \Leftarrow C \Leftrightarrow A \Leftrightarrow B \Leftrightarrow E$$.  But the above ignores time.  

Getting even more general, each of the above random variables could be indexed by individual.  In this case, the body $$behavior$$ of one individual can impact both the activity $$A$$ and environment $$E$$ of another.   To further complicate things, the individuals are further connected by genetics, $$D$$.  For example, the genome $$D$$ of an individual in one generation is highly dependent on the genomes of two other individuals (her parents). And, of course, all this is happening in time, so each variable for each individual could be indexed by time (except the somatic genome, which is constant within an individual).






a connectome is the mechanism that the genome uses to encode its desired behavioral statistics,
which, when combined with the rules of physics governing dynamics and physiology,
may be sufficient.
