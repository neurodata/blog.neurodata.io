---
layout: post
title:  "Connectome Coding"
date:   2018-08-29 14:27:57 -0400
tags: [brains, bits]
author: Joshua Vogelstein
---

The following are notes based first on an invited talk I gave at [Baylor](http://dx.doi.org/10.6084/m9.figshare.1140321), and then a [tutorial](https://neurodata.io/talks/sfn17.html) I gave at the Society for Neuroscience in 2017.  More recently, I was asked to write an article for [Current Opinion in Neurobology](https://www.sciencedirect.com/journal/current-opinion-in-neurobiology), which will be based largely on this blog post. This content flowed most recently from conversations with [Brett Mensh](http://optimizescience.com/) and [Carey E. Priebe](https://www.ams.jhu.edu/~priebe/), who will be co-authors on the resulting manuscript. I presented a slide version of these contents at the [Functional, Structural, and Molecular Imaging, and Big Data Analysis](http://www.sfn.org/-/media/SfN/Documents/NEW-SfN/Careers/2018/Career-Tools-and-Resources/Scientific-Short-Courses/SC2-Agenda-FINAL.pdf?la=en&hash=312E38148FDCC38DFB27811404404E9250BD80C5) Short Course at SfN in 2018.

---------------



The word "connectome" was coined in 2005  by both 
Professor Olaf Sporns and Dr. Patric Hagmann. 
They both independently defined the connectome, essentially, as a brain network. A network  is defined by two sets: a set of nodes (or vertices, or actors), and a set of edges (or arcs, or connections) between those nodes. As of November 2018, a PubMed search reveals XXX studies mentioning the word "connectome".  The word, and the field, have  evolved significantly  in these past 13 years.  In this opinion piece we introduce and formalize the concept of a `connectome code`, bringing together both historical and contemporary studies of connectomics, and providing a paradigm to help guide future studies.  We introduce the concept of a connectome code by defining a number of terms. 


## What is a Code?



`
A code is a system of (potentially stochastic) rules that translate from one representation of information into another.  
`

An example is the morse code, which is a system of rules that translate tones, lights, or clicks to alphanumeric characters. The morse code happens to be deterministic and "oneto-one" meaning that each sequence of beeps tranlate into a single character, and vice versa.   The genetic code translates nucleotide triplets into amino acids.  The genetic code is also deterministic, but it is not one-to-one, because multiple triplets encode the same nucleotide.  The neural code translates between neural activity (typically spiking activity) and sensory input or motor output.  This code is probabilistic, meaning that many different patterns of activity can encode the same stimulus or behavior, and a stimulus or behavior can elicit many different neural activity patterns. We are interested here in a different kind of code, which probabilistic governs connectomes. 



## What is a Connectome?




`A connectome is a network of a brain, at a particular spatiotemporal precision and extent. The nodes are distinct biophysical entities with three-dimensional (3D) morphological boundaries (not necessarily contiguous). The edges are either: (1) structural, meaning they are physical morphological objects, or they are (2) functional, meaning they characterize the statistical and/or causal relationship between the activity of a pair of nodes. `  

The above definition implies that a given brain could have many different connectomes, at different times, or at different resolutions, or both.  It also suggests that we measure properties of the brain, and use them  to *estimate* connectomes, and therefore our estimates necessarily are noisy and imperfect. When estimating a connectome, one must choose a construct for both the nodes and the edges. 

The mechanisms of defining and estimating a node are quite variable, and include using basic anatomy, functional activity, and connectivity. For example, a node can be a neuron, or an anatomical brain region, or a set of voxels in a brain that respond in a particular fashion to a particular set of stimuli.  Moreover, each node is *labeled*, that is, it corresponds to a specific entity which often has a corresponding entity in any other typical  organism of the same species.  This is in stark contrast to a "network" as defined in graph theory, where nodes labels, or any biophysical properties such as locations and shapes.  In connectomics, one can choose to ignore these node attributes when doing the analysis if one so chooses (which is the norm), but there is no way to estimate a connectome without addressing these considerations. 

The mechanisms of defining and estimating the edges of connectomes are even more variable, as suggested by the fact that there are two commonly used "types" of edges: structural and functional. Structural edges are physical connections between a pair of nodes, such as  synapses connecting a pair of neurons, or a set of fiber bundles  connecting a pair of anatomical regions.  Functional edges characterize statistical and/or causal relationships between the activity of a pair of nodes, such as (Pearson's) correlation between a pair of regions, or estimated connection strength within a generalized linear model characterizing neural spiking activity. In classical graph theory, there are no types of edges, they  are binary, and otherwise lack attributes such as physical extents, or underlying statistical models. Cne can  "binarize" an estimate of a connectome's edges (converting weights into 0's or 1's depending on whether they are above or below a particular threshold), and discard other information as well (how the edge was defined), but one need not do so. 

Note that we have not limited the definition of a connectome to be comprehensive, because the concept of being comprehesive is not philosophically tenable.  Once can define the connectome at a particular spatial resolution and temporal extent, for example, every neuron in the brain is a node, and the chemical synapses at a given time are the edges. But then referring to it as comprehensive is a bit vacuous, as it is only comprehensive relative to the imposed constraints, and everything is comprehensive with respect to some constraints.  Thus, there is no such thing really as a comprehensive connectome, even for an individual.  This is in stark contrast to an individual's *somatic* genome, which is the genetic sequence of the mother cell of the individual. In genomics, each person really does have a single genome, and one can, in theory, estimate it with high accuracy.  

Based on the above definitions, any study or description of neural circuitry can be considered a study or description of a connectome.  Moreover, because connectomes fundamentally have network, node, and edge attributes, choosing which properties of the brain to include in the description of a connectome is a matter of choice.  In this sense, nodes can be more abstract, for example, corresponding to a "type" of neuron.  Moreover, node and edge attributes can be more complex, such as current gene expression profile of a node, or the number and location of vesicles in a synapse. Thus, while historically, studies on the somatoganglion circuit of a crab, or the sound localization circuit of a barn-owlm were not considered connectomics (at least partially because the word did not exist), given these modern definitions, we can and do consider them fundamental results in connectomics.  In fact, any study or description of the structure of the brain that includes a characterization of connections between pairs of nodes, regardless of the level of complexity or abstraction, can rightly be considered connectomics. 


## What is the Connectome Code?


`A connectome code is system of (potentially stochastic) rules that translate to and from connectomes.`

The above definition begs the question of what a connectome can be translated to or from.   To answer this question we provide a conceptual model which links brains, bodies, and worlds in a nested set of intertwined spiral loops.   

(see below image). 

![brain body world](/assets/post_images/brain-body-world.png)
*Image Credits: [Julia Kuhl](http://somedonkey.com/) and [Brett Mensh](http://optimizescience.com/)*

Worlds contain bodies which contain brains. And brains are composed of both structure (which we think of as basically static) and activity (which we think of as basically dynamic).  The structure and activity are inextricably linked in an inner feedback loop that operates on fast and small scales (seconds and microns): the structure provides biophysical statistical rules governing the activity, and activity results in plasticity which changes the structure.  The joint role of the structure and activity (i.e., the brain) is to direct the body's motor control, so that it behaves in the world in certain ways, driving an middle feedback loop that operates at moderate time and spatial scales (minutes and centimeters).  This middle feedback look connects the behaviors of the animal to its sensory input, including both egocentric  (e.g., proprioception) and allocentric  (e.g., vision) sensory input.  The world, and specifically the niche in which a given animal resides, exterts selective pressures on those behaviors in an outer loop with even slower and larger scales (generations and meters). The behaviors that tend to increase the "fitness" of the organism survive to the next generation, whereas the behaviors that tend to decrease the fitness of the organism are eliminated.  Thus, the organisms with relatively successful behaviors get to propagate their genomes to the next generation.  Those genomes provide the blueprint governing development, which starts the cycle all over again.  These intertwined loops are spiral because the cycles do not return to where they started, but rather start in a new (and hopefully improved) place. 

The implications of the above conceptual model, with respect to connectome coding, is that  **the connectome is the mechanism by which the genome can encode its preferred behaviors, that, when combined with the body (and physics) yields the desired behaviors with sufficiently high probability to help the organism win the evolutionary game its niche imposes on it.**    In this sense, a genome encodes a connectome (and its dynamics via the rules of plasticity), and a connectome at any given time encodes the probability of various self-driven or responsive behaviors.  There are therefore two kinds of connectome coding rules: 
1. connectome encoding rules convert genomes into dynamic connectomes, and 
2. connectome decoding rules convert connectomes into behaviors. 


### A Statistical Formalization of Connectome Coding


<!-- that given random variable $$X$$ takes some value from its set of possible values $$x \in \mathcal{X}$$,  that $$Y$$ takes any of its possible values, $$y \in \mathcal{Y}$$.  In other words, $$P[Y \vert X]$$ is the probabilistic rule converting from $$x$$ to $$y$$.  -->
<!--  happending.  -->


In the language of statistics, a code is a conditional distribution which characterizes the probability of an event conditioned on some other event. For example, let $$X$$ and $$Y$$ be random variables, then $$P[Y \vert X]$$ characterizes the probability that $$Y$$ takes a particular value given that $$X$$ is some value, and we can define $$P[X \vert Y]$$ similarly.  The art and practice of connectome coding  therefore concerns estimating the statistical relationships between connectomes and  genomes/behaviors.  


We therefore statistically model each component of the above conceptual model as follows:  
- $$A$$ denotes brain activity, 
- $$B$$ denotes a set of behaviors, 
- $$C$$ denotes a connectome, 
- $$D$$ denotes genome (whose mechanism of action is development), and  
- $$E$$ denotes the world (or environment). 
  
Letting each of $$A,B,C,D,E$$ be random variables, a connectome code is a conditional distribution that characterizes the probability of some of the above variables taking any possible value, conditioned on the value of the other variables. 

To be more concrete, first, consider $$P[C \vert D]$$, which specifies the probability of an individual having a specific connectome, conditioned on her genome (via development).  In other words, in this model, the genome must *encode* the probabilistic rules of connectivity, at some resolution, to ensure that the connectome can function sufficiently well in the expected environmental niche in which the organism lives.  Second, consider $$P[A,B,E \vert C]$$, which specifies the probability  of an organisms brain activity, her behaviors, and its environment, conditioned on any  particular connectome.  One can also consider $$P[A \vert C]$$, or $$P[B \vert C]$$, or $$P[A,B \vert C]$$, etc.  Given the full joint distribution, $$P[A, B, C, D, E]$$, any of the above conditional and marginal distributions are mathematically available.   

The above probabilistic description does not incorporate the concept of causality.  However, our conceptual model does assert a causal structure.   Specifically, letting $$i$$ denote a generation, our conceptual model asserts $$D_i \Leftarrow C_i \Leftrightarrow A_i \Leftrightarrow B_i \Leftrightarrow E_i \Rightarrow D_{i+1}$$, further suggesting the spiral structure.  One of the implications of this causal dependence structure is that for the genome to encode the probabilistic rules of behavior to facilitate the organism winning the evolutionary game, it **must** go "through" the connectome. In other words, formalizing our conceptual model provides another perspective on the role of connectome codes: the causal mechanism connecting  genes to brain activity and behavior requires going through a connectome.   Since behavior is ongoing, dynamic, and responsive to the environment, and the somatic genome is static, the genome must essentially encode a blueprint that *guides* the construction of a vessel whose physical properties are such that they encourage "high value" behaviors.  That vessel is the connectome.  


This view of connectomes, and connectome coding, is, to our knowledge, essentially novel.  That said, it is a conceptual and formal model that one can use to interpret any previous study of connectomics.  Perhaps more important, we hope it will help guide the development and ideation of new connectomic studies, by providing a paradigm within which to ask and formalize questions about neural circuit mechanisms, how they work, how they fail, and how they can be improved.  