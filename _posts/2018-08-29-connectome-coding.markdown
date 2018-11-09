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
They  independently defined the connectome, essentially, as a brain network. Any network  is defined by two sets: a set of nodes (or vertices, or actors), and a set of edges (or arcs, or connections) between those nodes. As of November 2018, a PubMed search reveals >3000 studies mentioning the word "connectome".  The word, and the field, have  evolved significantly  in these past 13 years.  In this opinion piece we introduce and formalize the concept of a `connectome code`, bringing together both historical and contemporary studies of connectomics, and providing a formal statistical paradigm to help guide future studies.  




## What is a Connectome?




`A connectome is a network of a brain, at a particular spatiotemporal precision and extent. The nodes are distinct biophysical entities with three-dimensional morphological boundaries (not necessarily contiguous). The edges are either (1) structural, meaning they are physical morphological objects, or  (2) functional, meaning they characterize the statistical and/or causal relationship between the activity of a pair of nodes. `  

The above definition implies that a given brain could have many different connectomes at different times, or at different resolutions, or both.  It also suggests that we measure properties of the brain, and use them  to *estimate* connectomes, and therefore our estimates necessarily are noisy and imperfect. When estimating a connectome, one must choose a construct and a data source for both the nodes and the edges; the data sources could and often are distinct. Both nodes and edges  can be defined  based on anatomy, activity, and/or connectivity. Any such choices impose constraints on the corresponding definitions and resolutions of the elements of the connectome. 


Nodes, for example, can be neurons, anatomical brain regions, or a set of voxels in a brain that respond in a particular fashion to a particular set of stimuli.  Moreover, each node is *labeled*, that is, it corresponds to a specific entity which often has a corresponding entity bilaterally, and can also have the "same" entity  in another  organism of the same species.   Edge definitions are even more variable, as evidenced by the fact that there are two commonly used "types" of edges: structural and functional. Structural edges are physical connections between a pair of nodes, such as  synapses connecting a pair of neurons, or a set of fiber bundles  connecting a pair of anatomical regions.  Functional edges characterize statistical and/or causal relationships between the activity of a pair of nodes, such as (Pearson's) correlation between a pair of regions, or estimated connection strength within a generalized linear model characterizing neural spiking activity.

#### Example Connectomes


We describe several different estimates of connectomes spanning the phylogenetic tree and spatiotemporal scales.  We will use these connectomes as working examples  to illustrate the power and flexibility of our proposed connectome coding framework. Figure 2 shows several different connectomes, to illustrate the flexibility of the concept of connectome.

![connectomes](/assets/post_images/fig_connectomes.png)
**Figure 2** Connectomes spanning four levels of the phylogenetic tree, each acquired using different experimental modalities and spatial resolutions, ranging from nanoscale (electron microscopy) to macroscale (MRI regions).  An adjacency matrix of a network shows the strength of connection between any pair of nodes.   The connectomes are depicted as weighted adjacency matrices; for the worm and human, the connectomes are multi-connectomes, with two different edge types, denoted by two different colors. In each case, the nodes are sorted by region.  Moreover, along each connectome we provide the degree sequence, that is, the sum of edge weights for each node. 
<!-- % @EB: consider adding the following:
1. update C. elegans with newer data
2. title of c. elegans should specify herm vs male.
% 2. adding male c elegans?
% 3. adding other drosophila dataset?
% 4. add region labels to x- and y-axes
% 5. make degree distributions conditional, eg, on type, or hemisphere, etc.?
% 6. update drosophila to have both left and right (in red and black), and make  both weighted.
% 7.  update mouse to also include Allan connectivity.
 -->

- **(A) Caenorhabditis elegans**	The  *Caenorhabditis elegans* (C. elegans) is the only animal that we have a complete, neuron-to-neuron level connectome. In the C. elegans connectome, edges are either chemical synapses or gap junctions.  Each edge's strength or weight corresponds to the number of synapses between its parent neurons. There are two sexes of C. elegans, the male and hermaphrodite, with different numbers of neurons (the male has more, most of the neurons are shared between the two sexes, but not all).  These connectome estimates  are derived by cumbersome manual tracing of axons and dendrites, and identification of synapses, in nanoscale electron micrographs, and were updated by  Varshney et al. (2011) and  Bentley (2016). 
The neurons have multiple kinds of labels, including names, side (left  vs. right  vs. neither) and class  (sensory, internal, and motor). Figure  2(B) shows the hermaphrodite weighted multi-connectome, including both chemical (gray) and electrical (red)  synapses.  Note that chemical synapses are unidirectional, whereas electrical synapses are bidirectional.

- **(B) Drosophila melanogaster**	Eichler et al. (2017) published a complete larval Drosophila connectome of both the left and right mushroom body, also derived from serial electron microscopy, using only chemical synapses. These edges are weighted (based on  counting the  number of synapses between a pair of neurons), and  directed.
	Neurons are categorized  into  kenyon cells (K), input neurons (I), output neurons (O), and projection neurons (P).  Figure  2(B) shows both the left and right mushroom bodies. Edges are both weighted and directed.
     <!--@eb: are there loops?  -->
<!-- %	\item The mouse microscale connectome from the Allen Institute was estimated using light microscopy tracer studies averaging $\approx 1000$ brains \cite{Oh2014}. The nodes of this network are neuroanatomical regions based on the Allen Reference Atlas  ontology. The resulting network is a directed and weighted network,  where the weight from region $u$ to $v$ correspond to the number of fluorescent voxels in region $v$ whose source neurons are in region $u$, normalized by the size of region $u$ (Figure  2(B)). -->

- **(C) Mus musculus**    Calabrese et al. (2015) generated a high-resolution connectivity estimate using ex vivo diffusion magnetic resonance imaging (dMRI).  This network is undirected, as dMRI lacks directional information, and weights correspond to the number of tracts estimated to go from one region to another. Because we do not know the mapping between  the absolute magnitude of  connection weights to any  physical connection, we rescale these weights to be between zero and one, and depict them in Figure  2(C) on a log scale.    Regions in the mouse  connectome can  be  partitioned into ``superstructures'', including frontal (F), hindbrain (H), midbrain (M), and white matter (W).
     
- **(D) Homo sapiens**  The Consortium for Reliability and Reproducibility collects multiple measurements of functional resting-state (F),  anatomical (A),  and/or diffusion (D) magnetic resonance imaging per individual. The  functional connectomes are Pearson correlation matrices, which have been converted to ranks, and then normalized between zero and one,  because such a representation has been shown to be more reliable than raw or thresholded correlations \cite{reliability}.  The diffussion connectomes are normalized as described above for the mouse.  The above multi-connectome estimate is derived from averaging the entire dataset consisting of 3,067 dMRI and 1,760 fMRI connectomes.  Of the many possible brain parcellations, each defining nodes differently, we elected to  use the Desikan parellation, assigning each cortical region into lobes including frontal (F),  occiptal (O), parietal (P), and temporal (T), as well as sub-cortical structures (S).




#### What is and what is not, Connectomics?

In classical graph theory, nodes have no labels or other attributes, and neither do edges (including weights).  Thus, commonly in connectomics the node labels, edge weights, and other properties are discarded during the analysis.  Note, however, that
there is no way to estimate a connectome without making decisions about which properties to incorporate, even if one can ignore them in the downstream analysis. Such properties need not be ignore in studies of connectomes. However, the existing set of tools commonly used in connectomics does not incorporate these properties, and thereby motivating extending the standard network analysis toolbox. 


Note that we have not limited the definition of a connectome to be comprehensive, because the concept of being comprehesive is not philosophically tenable.  Once can define the connectome at a particular spatial resolution and temporal extent, for example, every neuron in the brain is a node, and the chemical synapses at a given time are the edges. Because connectomes fundamentally have network, node, and edge attributes, choosing which properties of the brain to include in the description of a connectome is a matter of choice.  Moreover, node and edge attributes can be more complex, such as current gene expression profile of a node, or the number and location of vesicles in a synapse. But then referring to it as comprehensive is a bit vacuous, as it is only comprehensive relative to the imposed constraints, and everything is comprehensive with respect to some constraints.  Thus, there does not exist a comprehensive connectome, even for an individual at a particular time.  This is in stark contrast to an individual's *somatic* genome, which is the genetic sequence of the mother cell of the individual. In genomics, each person really does have a single genome, and one can, in theory, estimate it with high accuracy.  For this reason, calls to measure the "complete connectome" demand further elaboration and justification. 

One final distinction is warranted given previous studies of anatomy and neural circuitry.  Typically, anatomical studies do not include studying connections between nodes, rather, they focus on the properties of each individual node.  That said, connectomics, as mentioned above, requires some aspect of anatomy to define its nodes.  Therefore, while all anatomical studies are not connectomics, all connectomics studies include anatomy.  Similarly, it is not the case that all studies of neural circuitry are connectomics.  In typical neural circuit investigations, the nodes are not distinct morpholical objects, rather, they are abstractions, such as "all pyramidal cells in layer 4". In this sense, not all studies of neural circuitry are connectomics, however, any study of connectomes may hope to reveal statistical principles that govern neural circuits.  For example, studies on the somatic ganglion circuit of a crab, or the sound localization circuit of a barn owl were not  connectomics.  However, one could imagine a connectomics study of the same circuitry would reveal the same underlying principles.  


## What is a Code?



`
A code is a system of (potentially stochastic) rules that translate from one representation of information into another.  
`

An example is the morse code, which is a system of rules that translate tones, lights, or clicks to alphanumeric characters. The morse code happens to be deterministic and "one-to-one" meaning that each sequence of beeps tranlate into a single character, and vice versa.   The genetic code translates nucleotide triplets into amino acids.  The genetic code is also deterministic, but it is not one-to-one, because multiple triplets encode the same nucleotide.  The neural code translates between neural activity (typically spiking activity) and sensory input or motor output.  This code is probabilistic, meaning that many different patterns of activity can encode the same stimulus or behavior, and a stimulus or behavior can elicit many different neural activity patterns. We are interested here in a different kind of code, which probabilistic governs connectomes. 



## What is the Connectome Code?


`A connectome code is system of (potentially stochastic) rules that translate to and from connectomes.`

The above definition begs the question of what a connectome can be translated to or from.   To answer this question we provide a conceptual model which links brains, bodies, and worlds in a nested set of intertwined spiral loops (see below image). 

![brain body world](/assets/post_images/brain-body-world.png)
*Image Credits: [Julia Kuhl](http://somedonkey.com/) and [Brett Mensh](http://optimizescience.com/)*

Worlds contain bodies which contain brains. And brains are composed of both structure (which we think of as basically static) and activity (which we think of as basically dynamic).  The structure and activity are inextricably linked in an inner feedback loop that operates on fast and small scales (seconds and (sub)cellular): the structure provides biophysical statistical rules governing the activity, and activity results in plasticity which changes the structure.  The joint role of the structure and activity (i.e., the brain) is to direct the body's motor control, so that it behaves in the world in certain ways, driving an middle feedback loop that operates at moderate time and spatial scales (minutes and organs).  This middle feedback look connects the behaviors of the animal to its sensory input, including both egocentric  (e.g., proprioception) and allocentric  (e.g., vision) sensory input.  The world, and specifically the niche in which a given animal resides, exterts selective pressures on those behaviors in an outer loop with even slower and larger scales (generations and whole bodies). The behaviors that tend to increase the "fitness" of the organism survive to the next generation, whereas the behaviors that tend to decrease the fitness of the organism are eliminated.  Thus, the organisms with relatively successful behaviors get to propagate their genomes to the next generation.  Those genomes provide the blueprint governing development, which starts the cycle all over again.  These intertwined loops do not return to where they started, but rather start in a new (and hopefully improved) place, making them intertwined spirals, also known as helices. 

The implications of the above conceptual model, with respect to connectome coding, is that  **the connectome is the mechanism by which the genome can encode its preferred behaviors, that, when combined with the body (and physics) yields the desired behaviors with sufficiently high probability to help the organism win the evolutionary game its niche imposes on it.**    In this sense, a genome encodes a connectome (and its dynamics via the rules of plasticity), and a connectome at any given time encodes the probability of various self-driven or responsive behaviors.  There are therefore two kinds of connectome coding rules: 
1. connectome *encoding* rules translate from genomes to probabilities of any dynamic connectomes, and 
2. connectome *decoding* rules translate from connectomes to probabilities of behaviors. 


### A Statistical Formalization of Connectome Coding




In the language of statistics, a code is a conditional distribution which characterizes the probability of an event conditioned on some other event. We therefore statistically model each component of the above conceptual model as follows:  
- $$A$$ denotes brain activity, including spiking activity, as well as sub-threshold voltage fluctuations, G-protein coupled receptor activity, gene expression dynamics, etc.,
- $$B$$ denotes a set of behaviors, including external behaviors such a running, and internal behaviors such as swallowing and breathing,
- $$C$$ denotes a connectome, as defined above,
- $$D$$ denotes the somatic genome (whose mechanism of action is development), and  
- $$E$$ denotes the world (or environment). 
  
Letting each of $$A,B,C,D,E$$ be random variables, a connectome code is a conditional distribution that characterizes the probability of some of the above variables taking any possible value, conditioned on the value of the other variables. Formally,  if $$X$$ and $$Y$$ are random variables, then their *marginal* distributions $$P[X]$$ and $$P[Y]$$ characterize the probability of any particular $$x$$ or $$y$$, 
and their *joint* distribution $$P[X,Y]$$  characterizes the probability of observing both $$x$$ and $$y$$.   The *conditional* distribution $$P[Y \vert X]$$ characterizes the probability that $$Y$$ takes a particular value given that $$X$$ is some value, and we can define $$P[X \vert Y]$$ similarly.  The art and practice of connectome coding  therefore concerns estimating the statistical relationships between connectomes and  genomes or behaviors.  


To be more concrete, consider $$P[C \vert D]$$, which specifies the probability of an individual having a specific connectome, conditioned on her genome (via development).  In other words, in this model, the genome must *encode* the probabilistic rules of connectivity, at some resolution, to ensure that the connectome can function sufficiently well in the expected environmental niche in which the organism lives.  Alternately, consider $$P[A,B,E \vert C]$$, which specifies the probability  of an organisms brain activity, her behaviors, and  environment, conditioned on a  particular connectome.  One can also consider $$P[A \vert C]$$, or $$P[B \vert C]$$, or $$P[A,B \vert C]$$, etc.  Given the full joint distribution, $$P[A, B, C, D, E]$$, any of the above conditional and marginal distributions are mathematically available.   

The above probabilistic description does not incorporate the concept of causality.  However, our conceptual model does assert a causal structure.   Specifically, letting $$i$$ denote a generation, our conceptual model asserts $$D_i \Leftarrow C_i \Leftrightarrow A_i \Leftrightarrow B_i \Leftrightarrow E_i \Rightarrow D_{i+1}$$, further suggesting the spiral structure.  One of the implications of this causal dependence structure is that for the genome to encode the probabilistic rules of behavior to facilitate the organism winning the evolutionary game, it must go "through" the connectome. In other words, formalizing our conceptual model provides another perspective on the role of connectome codes: the causal mechanism connecting  genes to brain activity and behavior requires going through a connectome.   Since behavior is ongoing, dynamic, and responsive to the environment, and the somatic genome is static, the genome must essentially encode a blueprint that *guides* the construction of a vessel whose physical properties are such that they encourage "high value" behaviors.  That vessel is the connectome.  


This view of connectomes, and connectome coding, is, to our knowledge, essentially novel.  That said, it is a conceptual and formal model that one can use to interpret any previous study of connectomics.  Perhaps more important, we hope it will help guide the development and ideation of new connectomic studies, by providing a paradigm within which to ask, formalize, and eventually questions about neural circuit mechanisms, how they work, how they fail, and how they can be improved.  