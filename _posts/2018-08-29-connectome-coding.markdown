---
layout: post
title:  "Connectome Coding: Discovering the Missing Link between Genotypes and Phenotypes"
date:   2018-08-29 14:27:57 -0400
tags: [brains, bits]
author: Joshua Vogelstein
---

# Abstract

The primary mechanism by which a genome can encode successful behaviors is via a developmental program that, when combined with environmental interactions, yields a particular brain structure from which successful behaviors tend to emerge. A critical aspect of brain structure is the number and distribution of types of "nodes" (where nodes could be neural compartments, neurons, or regions of interest, each with specific morpho-molecular properties), and the distribution of connections among them. "Connectal coding", by way of analogy with neural (activity) coding, is the art, study, and practice of inferring from data which aspects of brain structure (in particular, the connections between nodes) (1) give rise to which aspects of behaviors, and (2) are determined by which aspects of the genome. These "connectotypes" are a key link from genotype to behaviotype. In this manuscript, we flesh out the above argument, compare and contrast it to the standard paradigm in systems neuroscience—neural coding—and suggest a formal statistical framework for connectal coding.

# A Scientific Model

The goal of this manuscript is to introduce and motivate, from first principles, an approach to studying the brain which we call connectal coding. Connectal coding is a mode of investigating the brain that is parallel and complementary to neural (activity) coding. Neural coding is the art, study, and practice of inferring from data the relationship between neural activity, and either stimuli or responses (both neural and behavioral) [[1]](https://paperpile.com/c/vMMsj6/l3UU). Neural coding is well established and widely accepted as a (possibly _the_) legitimate framework for studying the brain. Connectal coding, on the other hand, is in its infancy, and therefore requires some motivation if researchers are going to take it seriously as an equally important framework for studying the brain. Therefore, to motivate connectal coding, we introduce the _connectal coding model_. 

## Connectal Coding Model

Any scientific model consists of (1) entities, with (2) properties and (3) causal activities, which are collectively (4) organized together to result in some phenomenon of interest [[2]](https://paperpile.com/c/vMMsj6/PQqc). In that sense, any mechanism is a "circuit", in which the entities are the nodes, and the causal activities characterize the connections. Our model—the _connectal coding model (CCM)_--is a simple model designed to explain how animals survive in the environment. CCM consists of four kinds of entities: genomes, brains, bodies, and worlds. Below we describe the properties and activities of each entity that are relevant for connectal coding.

* The genome is the germline genome — which is fixed at birth of the individual — consists of the set of genes that participate in development. The genome's activity is the developmental program, and specifically the neural developmental program, which gives rise to brain properties, in conjunction with interactions with the world [[3]](https://paperpile.com/c/vMMsj6/XRXb). 
* The brain's properties of interest are the number and distribution of types of "nodes"  (which may correspond to sub-cellular compartments, cells, regions, or other objects, each with specific morpho-molecular properties), and the distribution of connections among them. The set of nodes and connections we refer to as the "connectome", for reasons explained below [[4,5]](https://paperpile.com/c/vMMsj6/vJyY+l9Ws). The activity of the connectome could include spiking and sub-threshold activity, as well as gene expression. These activities result in both activity dependent plasticity, modifying various brain properties (including connectivity), as well as activating muscle cells. 
* The body's properties are those muscle cells, and the corresponding parts that participate in behavior [[6]](https://paperpile.com/c/vMMsj6/gmYb). 
* The world is simply the environment of the individual. For the purposes of CCM, we leave its properties quite vague. Its activities are selective pressures, which can result in either survival or elimination of the individual at any given time. 

The implications of this model are that for an individual to thrive in a given environment requires that she exhibits certain behaviors with sufficiently high probability. Moreover, for a parent to increase her offsprings' ability to thrive, she must communicate to them which behaviors tend to enable survival. The most effective strategy for communicating these proclivities is by providing a genome whose resulting developmental program tends to result in a connectome whose activities tend to lead to those behaviors in those circumstances. Importantly, the above model is agnostic with regards to which level of mechanism is the most appropriate for any given behavioral phenomenon; rather, the key is at any given level, the description includes a connectome.

![connectal coding](images/connectal-coding.jpg "connectal coding")
**_Figure 1: The Connectal Coding Model. Image Credits: [Julia Kuhl](http://somedonkey.com/) and [Brett Mensh](http://optimizescience.com/)_**

# The Connectome as a Model of the Brain

The Brain is a complex multiscale physical object with myriad sub-parts and properties. We refer to this structure as the connectome, rather than simply "brain anatomy" or "brain structure" to emphasize the importance of connectivity in the CCM model. As mentioned above, we are agnostic as to which level of entity "node" refers to, and could include, neural compartments, or neurons, or entire regions of interest. We and others, however, anticipate that the key to explaining various mental phenomenon, including both cognitive function and dysfunction, will be the strength (or weakness) of connectivity between certain pairs of"nodes". To provide two key examples, the engram — the set of physical processes and changes in the brain store memories — is widely conjectured to be distributed across a network of cells [[7–9]](https://paperpile.com/c/vMMsj6/ZAig+qfQi+DOQe). Moreover, an increasingly common view of psychiatric and neurological disorders is that they are etiologically "connectopathies" [[10,11]](https://paperpile.com/c/vMMsj6/dkjE+yxUx). The word "connectome" was independently coined in 2005 by both Professor Olaf Sporns and Dr. Patric Hagmann. Sporns defined the connectome as "a comprehensive structural description of the network elements and connections forming the human brain".

The above discussion leverages the concept from graph theory of a network, or graph. Any network is defined by two sets: a set of nodes (or vertices, or actors), and a set of edges (or arcs, or connections) between those nodes [[12]](https://paperpile.com/c/vMMsj6/4pjX). Some networks are directed, meaning that edges are directed from one node to another, but not necessarily vice versa. Other networks are undirected, such that communication flows freely in both directions. Some networks are weighted, meaning that associated with each edge is a "strength"; otherwise, the network is binary, so edges are only "on" or "off". Loops are allowed in some networks, meaning nodes can have edges with themselves. Finally, the graph, individual nodes, and edges may all have properties or attributes. For examples, nodes may have labels, corresponding to which groups they participate in.

Since the original definition of connectome, over 3000 publications have used the word, often times with different meanings. Below, we provide our definition, which is hopefully clear, concise, and inclusive:

    **Definition** A connectome is a network of a brain, at a particular spatiotemporal precision and extent. The nodes are biophysical (structural) entities such as neurons, Brodmann areas, or voxels. The edges are either (1) structural, meaning they are physical objects, or (2) functional, meaning they characterize the statistical and/or causal relationship between the activity of a pair of nodes. The connectome as a whole, as well as each node and edge can have a rich set of attributes. For example, the connectome can have an overall volume, nodes can have complex morphological shapes, and edges can be composed of many different proteins.

This definition implies that a given brain could have many different connectomes at different times, or at different resolutions, or of different types, etc. Given these choices, one can measure the parts of the brain to estimate a connectome. In genetics, the genotype corresponding to a given behavior is the set of genetic variants implicated in the behavior. In a similar fashion, the connectotype corresponding to a given behavior is the set of connectivity variants implicated in the behavior. Because these "behaviors" are not necessarily discrete motor patterns, but rather, are sets of responses to given stimuli, we refer to them here as behaviotypes [[13]](https://paperpile.com/c/vMMsj6/hEtc).

## Example Connectomes

Figure 2 shows several different connectomes, to illustrate the flexibility of the connectome concept. Each is estimated from a different species spanning from the simplest to most complex animals, with widely disparate definitions of what constitutes nodes and edges. There are many possible ways to visualize a connectome. We present a relatively simple way: adjacency matrices. The (u,v)<sup>th</sup> element of an adjacency matrix indicates the presence (or absence) of a connection from node u to node v. We indicate the strength of connection either as the size or contrast of the corresponding matrix element. Showing an adjacency matrix requires first sorting all the nodes in some order, we choose to sort the nodes by which region or type, but other sortings could be equally informative. For certain connectomes, experimentalists have measured multiple types of edges, we show these "multi-connectomes" with different colors for the different edge types.

![connectomes](images/connectomes.png "connectomes")
**_Figure 2: Connectomes spanning four levels of the phylogenetic tree, each acquired using different experimental modalities and spatial resolutions, ranging from nanoscale (electron microscopy) to macroscale (MRI regions). (A) C. elegans multi-connectome obtained from male and hermaphrodite connectomes. Nodes represent neurons, and are assigned into left (L) and right (R), which are bilateral pairs, as well as unpaired (U). Nodes are further assigned into endorgan neurons (E), interneurons (I), motor neurons (M), and sensory neurons (S). Size of circles correspond to the number of synapses between two neurons. (B) Left mushroom body connectome from Drosophila melanogaster. Nodes represent neurons, and are assigned into kenyon cells (KC), input neurons (MBIN), output neurons (MBON), and projection neurons (PN). Color intensity corresponds to the number of synapses between two neurons. (C) Mouse connectomes obtained from dMRI scans. Nodes represent regions of the brain, and are assigned into right (R) and left (L) hemispheres and then further assigned into frontal (F), hindbrain (H), midbrain (M), and white matter (W). Color intensity corresponds to to degree of connectivity between two regions. **(D) **Human multi-connectome obtained from averaging 3,067 dMRI and 1,760 fMRI human connectomes. Since both networks are undirected, only upper triangle of fMRI connectome and lower triangle of dMRI connectome is shown. Nodes represent regions of the brain, and are assigned into right (R) and left (L) hemispheres and then further assigned into frontal (F), occipital (O), parietal (P), and temporal (T), as well as sub-cortical structures (S). Color intensity corresponds to degree of connectivity and correlation for dMRI and fMRI, respectively, between two regions.**

1. **Caenorhabditis elegans** The Caenorhabditis elegans (C. elegans) is the only animal that we have a complete connectome where the nodes represent neurons [[14–16]](https://paperpile.com/c/vMMsj6/cELI+6Jjc+kzhl). It is complete in the sense that every neuron in the animal is a node, and every edge has been estimated. In this connectome, there are two types of edges corresponding to two types of neural activities: (1) chemical synapses, which correspond neurochemical release, and (2) gap junctions, which correspond to electrical activity. Each edge's strength (or weight) corresponds to the number of synapses between its parent neurons. There are two sexes of C. elegans, the male and hermaphrodite, with different numbers of neurons (the male has more, most of the neurons are shared between the two sexes, but not all) [[17,18]](https://paperpile.com/c/vMMsj6/VoIz+9XpI). These connectome estimates are derived by cumbersome manual tracing of axons and dendrites, and identification of synapses, in nanoscale electron micrographs, and were updated by Varshney et al. [[19]](https://paperpile.com/c/vMMsj6/4tZZ) and again by Bentley [[20]](https://paperpile.com/c/vMMsj6/GIMf). The neurons have multiple kinds of labels, including names, side (left vs. right vs. neither) and class (sensory, internal, and motor). Figure 2(A) shows the hermaphrodite weighted multi-connectome, including both chemical (gray) and electrical (red) synapses. Note that chemical synapses are unidirectional, whereas electrical synapses are bidirectional.
2. **Drosophila melanogaster** Eichler et al. [[21]](https://paperpile.com/c/vMMsj6/u2LZ) published a complete larval Drosophila connectome of both the left and right mushroom body, also derived from serial electron microscopy, using only chemical synapses. These edges are weighted (based on counting the number of synapses between a pair of neurons), and directed [[22]](https://paperpile.com/c/vMMsj6/8u1I). Neurons are categorized into kenyon cells (K), input neurons (I), output neurons (O), and projection neurons (P). Figure 2(B) shows both the left and right mushroom bodies. Edges are both weighted and directed.
3. **Mus musculus** Calabrese et al. [[23]](https://paperpile.com/c/vMMsj6/4Kti) generated a high-resolution connectivity estimate using ex vivo diffusion magnetic resonance imaging (dMRI). This network is undirected, as dMRI lacks directional information, and weights correspond to the number of tracts estimated to go from one region to another. Because we do not know the mapping between the absolute magnitude of connection weights to any physical connection, we rescale these weights to be between zero and one, and depict them in Figure 2(C) on a log scale. Regions in the mouse connectome can be partitioned into "superstructures", including frontal (F), hindbrain (H), midbrain (M), and white matter (W).
4. **Homo sapiens** The Consortium for Reliability and Reproducibility collects multiple measurements of functional resting-state (F), anatomical (A), and/or diffusion (D) magnetic resonance imaging per individual [[24]](https://paperpile.com/c/vMMsj6/P3yE). The functional connectomes are Pearson correlation matrices, which have been converted to ranks, and then normalized between zero and one, because such a representation has been shown to be more reliable than raw or thresholded correlations [[25]](https://paperpile.com/c/vMMsj6/s15T). The diffusion connectomes are normalized as described above for the mouse. The above multi-connectome estimate is derived from averaging the entire dataset consisting of 3,067 dMRI and 1,760 fMRI connectomes [[24]](https://paperpile.com/c/vMMsj6/P3yE). Of the many possible brain parcellations, each defining nodes differently, we elected to use the Desikan parcellation, assigning each cortical region into lobes including frontal (F), occipital (O), parietal (P), and temporal (T), as well as sub-cortical structures (S).

## What is and what is not, Connectomics?

In classical graph theory, nodes have no labels or other attributes, and neither do edges (including weights). Thus, commonly in connectomics the node labels, edge weights, and other properties are discarded during the analysis. Note, that there is no way to estimate a connectome without making decisions about which properties to incorporate, even if one can ignore them in the downstream analysis. However, the existing set of tools commonly used in connectomics does not incorporate these properties, thereby motivating extending the standard network analysis toolbox.

We have not limited the definition of a connectome to be comprehensive set of all nodes and edges, because the concept of being comprehensive is not philosophically tenable. Even given the constraints of a particular spatial resolution and extent, the connectome varies over time, and various attributes could or could not be incorporated into the definition. In this case, referring to it as comprehensive is a bit vacuous, as it is only comprehensive relative to the imposed constraints, and everything is comprehensive with respect to some constraints. Thus, there does not exist a comprehensive connectome, even for an individual at a particular time. This is in stark contrast to an individual's germline genome, which is the genetic sequence of the mother cell of the individual. In genomics, each person really does have a single genome, and one can, in theory, estimate it with high accuracy. For this reason, calls to measure the "complete connectome" demand further elaboration and justification.

Connectomics differs from both classical anatomical studies and studies of neural circuitry. Anatomical studies can, but need not, characterize connectivity. But, connectomics requires some aspect of anatomy to define its nodes. Therefore, while all anatomical studies are not connectomics, all connectomics studies include anatomy. Similarly, it is not the case that all studies of neural circuitry are connectomics. In typical neural circuit investigations, the nodes are not distinct morphological objects, rather, they are abstractions, such as "all pyramidal cells in layer 4". In this sense, not all studies of neural circuitry are connectomics, however, any study of connectomes may hope to reveal statistical principles that govern neural circuits. For example, studies on the somatic ganglion circuit of a crab [[26]](https://paperpile.com/c/vMMsj6/D5tV), or the sound localization circuit of a barn owl [[27]](https://paperpile.com/c/vMMsj6/DyqM) were not connectomics. However, one could imagine a connectomics study of the same circuitry would reveal the same underlying principles.

Finally, connectal coding does _not _require access to connectomes. Rather, it is a framework for thinking about explaining how the brain works, and modeling the data. Classical electrophysiological datasets can be used to infer connectotypes, and basic modeling can be used to propose them. Connectome data is there just one of many experimental paradigms that one can use for connectal coding, but certainly not the only.

## Connectal Coding as an Approach to Learn About Connectomes

To understand what connectal coding is requires understanding what a code is.

* **Definition** A code is a system of (potentially stochastic) rules that translate from one representation of information into another.

An example is the morse code, which is a system of rules that translate tones, lights, or clicks to alphanumeric characters. The morse code happens to be deterministic and "one-to-one" meaning that each sequence of beeps translate into a single character, and vice versa. The genetic code translates nucleotide triplets into amino acids. The genetic code is also deterministic, but it is not one-to-one, because multiple triplets encode the same nucleotide. The neural code translates between neural activity (typically spiking activity) and sensory input or motor output. This code is probabilistic, meaning that many different patterns of activity can encode the same stimulus or behavior, and a stimulus or behavior can elicit many different neural activity patterns. We are interested here in a different kind of code, which probabilistically governs connectomes.

* **Definition** A connectome code is system of (potentially stochastic) rules that translate to and from connectomes.

In this sense, a genome encodes a connectome (and its dynamics via the rules of plasticity), and a connectome at any given time encodes the probability of various self-driven or responsive behaviors. Like neural coding, there are two kinds of connectome coding rules:

1. connectome encoding rules translate from genomes to probabilities of (potentially dynamic) connectomes, and
1. connectome decoding rules translate from connectomes to probabilities of (potentially dynamic) behaviors.

One can therefore think of a connectal code as a mechanistic explanation of how the genome encodes certain behaviors. Some might argue that these are not "explanations", but rather descriptions, and explanations require some additional semantic content. We leave such discussions for other work, and focus the remainder of this article on formalizing these concepts.

## A Statistical Formalization of Connectome Coding

In the language of statistics, a code is a conditional distribution which characterizes the probability of an event conditioned on some other event. Statistical models consist of collections of random variables, each of which has parameters that govern its samples. Linking back to our approach to modeling, we say that each random variable is an "entity", its properties are the parameters of its distribution, and its activities are its potential realizations. The organization indicates which random variables are dependent on one another. Let W, X, Y, and Z be random variables, their marginal distributions P[W], P[X], P[Y], and P[Z] characterize the probability of any particular w, x, y, or z; and their joint distribution P[W,X,Y,Z] characterizes the probability of observing w and x and y and z. The conditional distribution P[Y|X] characterizes the probability that Y takes a particular value given that X is some value, and we can define other conditional distributions similarly. 

In connectal coding, based on the above model, we have the following four random variables:

* Z(i) = genome of subject i, activities are development, which act on brain i and body i
* Y(i) = brain of subject i, activities are neural and glial activations which act on brain i and body i
* X(i) = body of subject i, activities are behaviors which act on body i and world
* W = world, activities are selective pressures, which act on bodies

The art and practice of connectal coding therefore concerns estimating the statistical relationships between connectomes and genomes or behaviors. One implication of this model is that for the genome to encode the probabilistic rules of behavior to facilitate the organism winning the evolutionary game, it must go "through" the connectome. In other words, formalizing our conceptual model provides another perspective on the role of connectome codes: the connectome is the causal mechanism, the missing link, between genes and behaviors. To paraphrase, **connectal coding is the search of connectotypes that link genotypes to behaviotypes**. 

This view of connectomes, connectome coding, and connectotyping, is, to our knowledge, essentially novel. That said, it is a conceptual and formal model that one can use to interpret any previous study of connectomics. Perhaps more important, we hope it will help guide the development and ideation of new connectomic studies, by providing a paradigm within which to ask, formalize, and eventually questions about neural circuit mechanisms, how they work, how they fail, and how they can be improved.

## References

    1. [Johnson KO. Neural coding. Neuron. 2000;26: 563–566. Available: https://www.ncbi.nlm.nih.gov/pubmed/10896153](http://paperpile.com/b/vMMsj6/l3UU)


    2. [Craver C, Tabery J. Mechanisms in Science [Internet]. Spring 2017. Zalta EN, editor. The Stanford Encyclopedia of Philosophy. Metaphysics Research Lab, Stanford University; 2017. Available: https://plato.stanford.edu/archives/spr2017/entries/science-mechanisms/](http://paperpile.com/b/vMMsj6/PQqc)


    3. [Rubenstein J, Rakic P, editors. Neural Circuit Development and Function in the Healthy and Diseased Brain: Comprehensive Developmental Neuroscience [Internet]. 1 edition. Academic Press; 2013. Available: https://smile.amazon.com/Circuit-Development-Function-Healthy-Diseased-ebook/dp/B00CWBZPPA/ref=sr_1_6?ie=UTF8&qid=1548036809&sr=8-6&keywords=developmental+neurobiology](http://paperpile.com/b/vMMsj6/XRXb)


    4. [Sporns O, Tononi G, Kötter R. The human connectome: A structural description of the human brain. PLoS Comput Biol. 2005;1: e42. doi:10.1371/journal.pcbi.0010042](http://paperpile.com/b/vMMsj6/vJyY)


    5. [Hagmann P. From diffusion MRI to brain connectomics. EPFL; 2005; Available: https://infoscience.epfl.ch/record/33696](http://paperpile.com/b/vMMsj6/l9Ws)


    6. [Krakauer JW, Ghazanfar AA, Gomez-Marin A, MacIver MA, Poeppel D. Neuroscience Needs Behavior: Correcting a Reductionist Bias. Neuron. 2017;93: 480–490. doi:10.1016/j.neuron.2016.12.041](http://paperpile.com/b/vMMsj6/gmYb)


    7. [Lashley KS. In search of the engram. Symp Soc Exp Biol. 1950;4: 30.](http://paperpile.com/b/vMMsj6/ZAig)


    8. [Thompson RF. In search of memory traces. Annu Rev Psychol. annualreviews.org; 2005;56: 1–23. doi:10.1146/annurev.psych.56.091103.070239](http://paperpile.com/b/vMMsj6/qfQi)


    9. [Berlot E, Popp NJ, Diedrichsen J. In search of the engram, 2017. Current Opinion in Behavioral Sciences. 2018;20: 56–60. doi:10.1016/j.cobeha.2017.11.003](http://paperpile.com/b/vMMsj6/DOQe)


    10. [Toga AW, Thompson PM. Connectopathy in ageing and dementia. Brain. 2014;137: 3104–3106. doi:10.1093/brain/awu276](http://paperpile.com/b/vMMsj6/dkjE)


    11. [Scholtens LH, van den Heuvel MP. Multimodal Connectomics in Psychiatry: Bridging Scales From Micro to Macro. Biol Psychiatry Cogn Neurosci Neuroimaging. 2018;3: 767–776. doi:10.1016/j.bpsc.2018.03.017](http://paperpile.com/b/vMMsj6/yxUx)


    12. [Bollobas B. Modern Graph Theory [Internet]. 1st ed. Springer-Verlag New York; 1998. doi:10.1007/978-1-4612-0619-4](http://paperpile.com/b/vMMsj6/4pjX)


    13. [Vogelstein JT, Park Y, Ohyama T, Kerr RA, Truman JW, Priebe CE, et al. Discovery of brainwide neural-behavioral maps via multiscale unsupervised structure learning. Science. 2014;344: 386–392. doi:10.1126/science.1250298](http://paperpile.com/b/vMMsj6/hEtc)


    14. [White JG. Neuronal connectivity in Caenorhabditis elegans. Trends Neurosci. 1985;8: 277–283. doi:10.1016/0166-2236(85)90102-X](http://paperpile.com/b/vMMsj6/cELI)


    15. [White JG, Southgate E, Thomson JN, Brenner S. The structure of the nervous system of the nematode Caenorhabditis elegans. Philos Trans R Soc Lond B Biol Sci. 1986;314: 1–340. Available: https://www.ncbi.nlm.nih.gov/pubmed/22462104](http://paperpile.com/b/vMMsj6/6Jjc)


    16. [White JG, Southgate E, Thomson JN, Brenner S. The structure of the ventral nerve cord of Caenorhabditis elegans. Philos Trans R Soc Lond B Biol Sci. 1976;275: 327–348. Available: https://www.ncbi.nlm.nih.gov/pubmed/8806](http://paperpile.com/b/vMMsj6/kzhl)


    17. [Jarrell TA, Wang Y, Bloniarz AE, Brittin CA, Xu M, Thomson JN, et al. The connectome of a decision-making neural network. Science. American Association for the Advancement of Science; 2012;337: 437–444. doi:10.1126/science.1221762](http://paperpile.com/b/vMMsj6/VoIz)


    18. [Emmons SW. Neural Circuits of Sexual Behavior in Caenorhabditis elegans. Annu Rev Neurosci. 2018;41: 349–369. doi:10.1146/annurev-neuro-070815-014056](http://paperpile.com/b/vMMsj6/9XpI)


    19. [Varshney LR, Chen BL, Paniagua E, Hall DH, Chklovskii DB. Structural properties of the Caenorhabditis elegans neuronal network. PLoS Comput Biol. 2011;7: e1001066. doi:10.1371/journal.pcbi.1001066](http://paperpile.com/b/vMMsj6/4tZZ)


    20. [Bentley B, Branicky R, Barnes CL, Chew YL, Yemini E, Bullmore ET, et al. The Multilayer Connectome of Caenorhabditis elegans. PLoS Comput Biol. 2016;12: e1005283. doi:10.1371/journal.pcbi.1005283](http://paperpile.com/b/vMMsj6/GIMf)


    21. [Eichler K, Li F, Litwin-Kumar A, Park Y, Andrade I, Schneider-Mizell CM, et al. The complete connectome of a learning and memory centre in an insect brain. Nature. 2017;548: 175–182. doi:10.1038/nature23455](http://paperpile.com/b/vMMsj6/u2LZ)


    22. [Priebe CE, Park Y, Tang M, Athreya A, Lyzinski V, Vogelstein JT, et al. Semiparametric spectral modeling of the Drosophila connectome [Internet]. arXiv [stat.ML]. 2017. Available: http://arxiv.org/abs/1705.03297](http://paperpile.com/b/vMMsj6/8u1I)


    23. [Calabrese E, Badea A, Cofer G, Qi Y, Johnson GA. A Diffusion MRI Tractography Connectome of the Mouse Brain and Comparison with Neuronal Tracer Data. Cereb Cortex. 2015;25: 4628–4637. doi:10.1093/cercor/bhv121](http://paperpile.com/b/vMMsj6/4Kti)


    24. [Zuo X-N, Anderson JS, Bellec P, Birn RM, Biswal BB, Blautzik J, et al. An open science resource for establishing reliability and reproducibility in functional connectomics. Sci Data. 2014;1: 140049. doi:10.1038/sdata.2014.49](http://paperpile.com/b/vMMsj6/P3yE)


    25. [Kiar G, Bridgeford E, Roncal WG, Consortium for Reliability and Reproducibliity (CoRR), Chandrashekhar V, Mhembere D, et al. A High-Throughput Pipeline Identifies Robust Connectomes But Troublesome Variability [Internet]. bioRxiv. bioRxiv; 2018. p. 188706. doi:10.1101/188706](http://paperpile.com/b/vMMsj6/s15T)


    26. [Marder E, Bucher D, Schulz DJ, Taylor AL. Invertebrate central pattern generation moves along. Curr Biol. 2005;15: R685–R699. doi:10.1016/j.cub.2005.08.022](http://paperpile.com/b/vMMsj6/D5tV)


    27. [Carr CE, Konishi M. A circuit for detection of interaural time differences in the brain stem of the barn owl. J Neurosci. 1990;10: 3227–3246. Available: http://www.ncbi.nlm.nih.gov/pubmed/2213141](http://paperpile.com/b/vMMsj6/DyqM)

