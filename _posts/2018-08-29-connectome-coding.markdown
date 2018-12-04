---
layout: post
title:  "Connectome Coding: Discovering the Missing Link between Genotypes and Phenotypes"
date:   2018-08-29 14:27:57 -0400
tags: [brains, bits]
author: Joshua Vogelstein
---

<!-- title:  "Connectome Coding: Discovering the Connectotype linking Genotypes to Phenotypes"
title: “Connectotypes: The Missing Link Between Genotypes and Phenotypes”-->
<!-- need abstract, up to 125 words, possibly incorporating some of the below paragraph -->
<!-- To understand any system we define the parts and the interactions. any scientific description contains parts and interactions/causings.  networks are abstractions that explicitly deal with  -->
<!-- parts have states -->
<!-- Mechanisms are entities and activities organized such that they are productive of regular changes from start or set-up to finish or termination conditions.’ -->
<!-- A mechanism for a phenomenon consists of entities and activities organized in such a way that they are responsible for the phenomenon. -->
<!-- A mechanism for a phenomenon consists of entities (or parts) whose activities and interactions are organized in such a way that they produce the phenomenon.  -->
<!-- brenner says: only 2 things to learn about a nervous system: 1. how is it built, 2. how does it work. -->
<!-- british medical bulletin 29, 269-271, 1973. "isolate mutations affecting behavior of an animal and see what changes have been produced in the nervous system." -->
<!-- connectomics: you can learn about the unknown unknowns -->
<!-- we want to connect the genotype to the phenotype, via a connectotype. connectome coding is the art and practice of estimating the the connectotype linking a given genotype/phenotype pair. -->
<!-- understand the relationship between the chemical connectivity matrix and the adhesion protein gene expression matrix -->


#### Abstract

We propose that the vast majority of brain scientists are studying the wrong thing. The two primary goals in brain sciences is to understand how brains came to be, and how they enable their corresponding bodies to thrive.  These two aspects are characterized by the genotype and phenotype of the individual.  The missing link connecting the genotype to phenotype is not brain activity, but rather, brain structure.  Therefore, we advocate for a shift in focus from neural coding to connectome coding.  Specifically, we define connectome coding as the art and practice of discovering the connectotypes that link specific genotypes to specific phenotypes.





### A Scientific Model

The goal of this manuscript is to introduce and motivate from first principles an approach to brain science, which we call *connectome coding*. Our thesis rests on a model of how the brain helps  individuals survive and propagate their genes.  In our model the goal of the brain is to develop and function in such a way as to maximize the fitness of the individual harboring the brain. We define fitness as a multigenerational cost function, in which the most fit individuals enable their offspring to thrive even under selective pressures. The genome--the set of all genes---is the mechanism by which individuals are able to provide effective strategies to the next generation.   The brain---which we will model below---is the mechanism by which the genome is able to provide effective strategies to the body. In other words, for the genome to increase to probability of certain phenotypes, and decrease the probability of other phenotypes, it must include a neurodevelopmental plan that results in a brain whose activities lead to those behaviors with those probabilities.  In other words, specific genotypes lead to different distributions of phenotypes, and the brain is the interlocutor between those genotypes and phenotypes. The below figure and caption explain and define our model in greater detail.  



![brain body world](/assets/post_images/brain-body-world.png)
> **Figure 1**: Scientific explanations, causal models, and dynamic systems all share a kind of structure.  There are (1) parts, those parts have (2) properties and (3) activities which are (4) organized.  In the above conceptual model, the parts are the brain, body, and world.  The brain properties of interest is its structure (including its connectivity), and its activities include spiking and gene expression.  Body properties include limbs, and its activities include both voluntary (such as movements) and involuntary (such as hearbeats and sensations). World properties include the environment in which the body interacts, its activities include other bodies, the rotation of the earth, etc. Brain activity causal impacts bodies, and bodies causally impact brains and world.  But brains and world do not directly interact, rather, the body is the interlocutor. For each individual, the initial condition is her genome.    *Image Credits: [Julia Kuhl](http://somedonkey.com/) and [Brett Mensh](http://optimizescience.com/)*


### The Relationship Between Brains, Brain Structure, and Connectomes

Given that the brain is connecting phenotypes to genotypes, the next natural question is which aspects of the brain "store" that information.  


In other words, the genome encodes brain structure, and therefore, it is brain structure---and not brain activity---that is the mechanism that the genome uses to provide instructions to future generations.  In fact, the only way for the genome to encourage particular kinds of brain activities, is via developmental programs that cause certain kinds of brain structures. 

Brain structure plays a crucial role in the above model: it is the missing link between the genome and desired behaviors.  The connectome, as elaborated upon below, is our scientific model of brain structure.   The word "connectome" was independently coined in 2005  by both Professor Olaf Sporns and Dr. Patric Hagmann. Sporns defined the connectome as  "a comprehensive *structural* description of the network elements and connections forming the human brain" (emphasis added).  The connectome, according to this definition, is the brain structure, and it crucially includes  connections between the elements.  This is in stark contrast to typical discussions of anatomy, in which various morphological and functional properties of individual brain elements may be studied, but rarely connections between those elements.  Since the original definitions, over 3000 publications have used the word "connectome", and its meaning has expanded.  Below, we provide our definition, which is an attempt to be as clear and concise and specific as possible, while incorporating a wide net of its current usage.

<!-- They  independently defined the connectome, essentially, as a brain network. Any network  is defined by two sets: a set of nodes (or vertices, or actors), and a set of edges (or arcs, or connections) between those nodes. As of November 2018, a PubMed search reveals >3000 studies mentioning the word "connectome".  The word, and the field, have  evolved significantly  in these past 13 years.  In this opinion piece we introduce and formalize the concept of a *connectome code*, bringing together both historical and contemporary studies of connectomics, and providing a formal statistical paradigm to help guide future studies.   -->

* **Definition** *A connectome is a network of a brain, at a particular spatiotemporal precision and extent.  The nodes are biophysical (structrual) entities such as neurons, Brodmann areas, or voxels. The edges are either (1) structural, meaning they are physical  objects, or (2) functional, meaning they characterize the statistical and/or causal relationship between the activity of a pair of nodes. The connectome as a whole, as well as each node and edge can have a rich set of attributes comprising its state space.  For example, the connectome can have an overall volume, nodes can have complex morphological shapes, and edges can have many different proteins.*

Linking back to the above approach to scientific explanation, we can therefore think of a connectome as a kind of explanation of the brain.  One first chooses the parts list and potential states of each part, and then chooses which kinds of causal processes are of relevance.  The connectome then characterizes the organization, that is, which parts interact with which other parts.  Since causal relations are sometimes too difficult to reliably estimate, researchers often use statistical relations as a surrogate.  In the language of graph theory or network science, the parts are called *nodes*. When a pair of parts directly interacts with one another, we say an *edge* exists between them.  Edges can be directed (such as when they correspond to causal processes) or undirected (such as when they correspond to statistical relationships). Moreover, parts can interact with themselves, created self-loops.


Much like an individual's genotype characterizes the aspects of the genome that are relevant for a certain phenotype, the **connectotype** characterizes the aspects of the brain that are relvant for


Thus, the process of defining a  connectome requires making choices about both the parts (which comprise the nodes) and the causal processes (which comprise the set of possible edges). 
<!-- Nodes, for example, can be neurons, anatomical brain regions, or a set of voxels in a brain that respond in a particular fashion to a particular set of stimuli.  Moreover, each node is *labeled*, that is, it corresponds to a specific entity which often has a corresponding entity bilaterally, and can also have the "same" entity  in another  organism of the same species.   Edge definitions are even more variable, as evidenced by the fact that there are two commonly used "types" of edges: structural and functional. Structural edges are physical connections between a pair of nodes, such as  synapses connecting a pair of neurons, or a set of fiber bundles  connecting a pair of anatomical regions.  Functional edges characterize statistical and/or causal relationships between the activity of a pair of nodes, such as (Pearson's) correlation between a pair of regions, or estimated connection strength within a generalized linear model characterizing neural spiking activity. -->
<!-- The above definition  -->
This implies that a given brain could have many different connectomes at different times, or at different resolutions, or of different types, etc.  Given these choices,  one can measure specific properties of the brain that provide information the parts, their states, and interactions, and use those measurements  to *estimate* connectomes. These estimates, like all estimates,  are noisy and imperfect. 


#### Example Connectomes


Figure 2 shows several different connectomes, to illustrate the flexibility of the connectome concept. Each is estimated from a different species spanning from the simplest to most complex animals, with widely disparate definitions of what consistutes nodes and edges. 

![connectomes](/assets/post_images/fig_connectomes.png)
**Figure 2** Connectomes spanning four levels of the phylogenetic tree, each acquired using different experimental modalities and spatial resolutions, ranging from nanoscale (electron microscopy) to macroscale (MRI regions).  An adjacency matrix of a network shows the strength of connection between any pair of nodes.   The connectomes are depicted as weighted adjacency matrices; for the worm and human, the connectomes are multi-connectomes, with two different edge types, denoted by two different colors. In each case, the nodes are sorted by region.  Moreover, along each connectome we provide the degree sequence, that is, the sum of edge weights for each node. 

- **(A) Caenorhabditis elegans**	The  *Caenorhabditis elegans* (C. elegans) is the only animal that we have a complete connectome where the nodes represent neurons.  It is complete in the sense that every neuron in the animal is a node, and every edge has been estimated. In this connectome, there are two types of edges: chemical synapses or gap junctions.  Each edge's strength or weight corresponds to the number of synapses between its parent neurons. There are two sexes of C. elegans, the male and hermaphrodite, with different numbers of neurons (the male has more, most of the neurons are shared between the two sexes, but not all).  These connectome estimates  are derived by cumbersome manual tracing of axons and dendrites, and identification of synapses, in nanoscale electron micrographs, and were updated by  Varshney et al. (2011) and  Bentley (2016). 
The neurons have multiple kinds of labels, including names, side (left  vs. right  vs. neither) and class  (sensory, internal, and motor). Figure  2(B) shows the hermaphrodite weighted multi-connectome, including both chemical (gray) and electrical (red)  synapses.  Note that chemical synapses are unidirectional, whereas electrical synapses are bidirectional.

- **(B) Drosophila melanogaster**	Eichler et al. (2017) published a complete larval Drosophila connectome of both the left and right mushroom body, also derived from serial electron microscopy, using only chemical synapses. These edges are weighted (based on  counting the  number of synapses between a pair of neurons), and  directed.
	Neurons are categorized  into  kenyon cells (K), input neurons (I), output neurons (O), and projection neurons (P).  Figure  2(B) shows both the left and right mushroom bodies. Edges are both weighted and directed.

- **(C) Mus musculus**    Calabrese et al. (2015) generated a high-resolution connectivity estimate using ex vivo diffusion magnetic resonance imaging (dMRI).  This network is undirected, as dMRI lacks directional information, and weights correspond to the number of tracts estimated to go from one region to another. Because we do not know the mapping between  the absolute magnitude of  connection weights to any  physical connection, we rescale these weights to be between zero and one, and depict them in Figure  2(C) on a log scale.    Regions in the mouse  connectome can  be  partitioned into ``superstructures'', including frontal (F), hindbrain (H), midbrain (M), and white matter (W).
     
- **(D) Homo sapiens**  The Consortium for Reliability and Reproducibility collects multiple measurements of functional resting-state (F),  anatomical (A),  and/or diffusion (D) magnetic resonance imaging per individual. The  functional connectomes are Pearson correlation matrices, which have been converted to ranks, and then normalized between zero and one,  because such a representation has been shown to be more reliable than raw or thresholded correlations \cite{reliability}.  The diffussion connectomes are normalized as described above for the mouse.  The above multi-connectome estimate is derived from averaging the entire dataset consisting of 3,067 dMRI and 1,760 fMRI connectomes.  Of the many possible brain parcellations, each defining nodes differently, we elected to  use the Desikan parellation, assigning each cortical region into lobes including frontal (F),  occiptal (O), parietal (P), and temporal (T), as well as sub-cortical structures (S).




#### What is and what is not, Connectomics?

In classical graph theory, nodes have no labels or other attributes, and neither do edges (including weights).  Thus, commonly in connectomics the node labels, edge weights, and other properties are discarded during the analysis.  Note, however, that
there is no way to estimate a connectome without making decisions about which properties to incorporate, even if one can ignore them in the downstream analysis. Such properties need not be ignore in studies of connectomes. However, the existing set of tools commonly used in connectomics does not incorporate these properties, and thereby motivating extending the standard network analysis toolbox. 


Note that we have not limited the definition of a connectome to be comprehensive, because the concept of being comprehesive is not philosophically tenable.  Once can define the connectome at a particular spatial resolution and temporal extent, for example, every neuron in the brain is a node, and the chemical synapses at a given time are the edges. Because connectomes fundamentally have network, node, and edge attributes, choosing which properties of the brain to include in the description of a connectome is a matter of choice.  Moreover, node and edge attributes can be more complex, such as current gene expression profile of a node, or the number and location of vesicles in a synapse. But then referring to it as comprehensive is a bit vacuous, as it is only comprehensive relative to the imposed constraints, and everything is comprehensive with respect to some constraints.  Thus, there does not exist a comprehensive connectome, even for an individual at a particular time.  This is in stark contrast to an individual's *somatic* genome, which is the genetic sequence of the mother cell of the individual. In genomics, each person really does have a single genome, and one can, in theory, estimate it with high accuracy.  For this reason, calls to measure the "complete connectome" demand further elaboration and justification. 

One final distinction is warranted given previous studies of anatomy and neural circuitry.  Typically, anatomical studies do not include studying connections between nodes, rather, they focus on the properties of each individual node.  That said, connectomics, as mentioned above, requires some aspect of anatomy to define its nodes.  Therefore, while all anatomical studies are not connectomics, all connectomics studies include anatomy.  Similarly, it is not the case that all studies of neural circuitry are connectomics.  In typical neural circuit investigations, the nodes are not distinct morpholical objects, rather, they are abstractions, such as "all pyramidal cells in layer 4". In this sense, not all studies of neural circuitry are connectomics, however, any study of connectomes may hope to reveal statistical principles that govern neural circuits.  For example, studies on the somatic ganglion circuit of a crab, or the sound localization circuit of a barn owl were not  connectomics.  However, one could imagine a connectomics study of the same circuitry would reveal the same underlying principles.  


### What is a Code?


* **Definition** *A code is a system of (potentially stochastic) rules that translate from one representation of information into another.*


An example is the morse code, which is a system of rules that translate tones, lights, or clicks to alphanumeric characters. The morse code happens to be deterministic and "one-to-one" meaning that each sequence of beeps tranlate into a single character, and vice versa.   The genetic code translates nucleotide triplets into amino acids.  The genetic code is also deterministic, but it is not one-to-one, because multiple triplets encode the same nucleotide.  The neural code translates between neural activity (typically spiking activity) and sensory input or motor output.  This code is probabilistic, meaning that many different patterns of activity can encode the same stimulus or behavior, and a stimulus or behavior can elicit many different neural activity patterns. We are interested here in a different kind of code, which probabilistic governs connectomes. 



### What is the Connectome Code?


* **Definition** *A connectome code is system of (potentially stochastic) rules that translate to and from connectomes.*

  In this sense, a genome encodes a connectome (and its dynamics via the rules of plasticity), and a connectome at any given time encodes the probability of various self-driven or responsive behaviors.  There are therefore two kinds of connectome coding rules: 
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

---------------

The above notes are based  on an invited talk I gave at [Baylor](http://dx.doi.org/10.6084/m9.figshare.1140321), and then a [tutorial](https://neurodata.io/talks/sfn17.html) I gave at the Society for Neuroscience in 2017.  More recently, I was asked to write an article for [Current Opinion in Neurobology](https://www.sciencedirect.com/journal/current-opinion-in-neurobiology), which will be based largely on this blog post. This content flowed most recently from conversations with [Brett Mensh](http://optimizescience.com/), [Carey E. Priebe](https://www.ams.jhu.edu/~priebe/), and Eric Bridgeford, who will be co-authors on the resulting manuscript. I presented a slide version of these contents at the [Functional, Structural, and Molecular Imaging, and Big Data Analysis](http://www.sfn.org/-/media/SfN/Documents/NEW-SfN/Careers/2018/Career-Tools-and-Resources/Scientific-Short-Courses/SC2-Agenda-FINAL.pdf?la=en&hash=312E38148FDCC38DFB27811404404E9250BD80C5) Short Course at SfN in 2018.



<!-- ------- -->


<!-- #### A Pedantic Model of the World -->

<!-- Our model consists of four components: (1) a description of the phenomenon of interest, (2) a list of entities and their corresponding properties, (3) a list of the causal activities governing the states and interactions of those entities, and (4) overarching organizing principles.  The below diagram schematizes our model, as elaborated below. The phenomenon we aim to explain is how individuals behave to thrive despite the selective pressures of the natural world.  In this context, thrive means to live long enough to pass one's genes to the next generation, and potentially engage in activities to support the development of next generation individuals. 
The entities engaged in this phenomenoon are nested: brains, bodies, world.  The brain properties of interest is its structure (including its connectivity), and its activities including spiking and gene expression.  Zooming out, body properties are limbs, and its activities include both voluntary (such as movements) and involuntary (such as hearbeats and sensations). The world properties include the environment in which the body interacts, its activities include other bodies, the rotation of the earth, etc. Brain activity causal impacts bodies, and bodies causally impact brains and world.  But brains and world do not directly interact, rather, the body is the interlocutor. These systems are dynamic, and dynamical systems depend on initial conditions.  For each individual, the initial condition is her genome.  In this model, the genome refers to the somatic genome of an individual, that is, the base-pair sequence of the first cell of that individual.  This genome provides the development plan, which is the blueprint for how the brain and body should develop and adapt. -->

<!-- Note that each of these causal activities operates in loops, that is, brain activity impacts brains and bodies, body activity impacts body and world, and world activity impacts body and world.  However, these are not quite loops, because they do  not return to where they started, but rather start in a new (and hopefully improved) place, -->

<!-- In addition to the above scales, initial conditions are required for any dynamical system. In this case, rather than characterizing the initial conditions of the entire system, we just state the initial conditions for a new brain/body pair: its genome. In this model, the genome refers to the somatic genome of an individual, that is, the base-pair sequence of the first cell of that individual.  This genome provides the development plan, which is the blueprint for how the brain should develop and adapt. -->




<!-- #### Phenonemon -->

<!-- <!-- great, but need to get to brain quicker —> -->

<!-- The phenomenon we aim to explain is how individuals behave to thrive despite the selective pressures of the natural world.  In this context, thrive means to live long enough to pass one's genes to the next generation, and potentially engage in activities to support the development of next generation individuals. -->



<!-- #### Entities


There are three entities that comprise the model:
1. **Brains**: For our purposes, brains are composed of cells. Each cell has a number of properties, including cell type (for example, neuron or glia), its three-dimensional morphological extent, its gene expression profile, its input-output curve, and its relative position in the brain.  Those cells interact with one another at chemical synapses and around gap junction. 
2. **Bodies**: Brains are inside bodies.  The bodies also have properties, including limbs, strength, organs, etc.
3. **World**: All the bodies are inside a world. The world has many properties, including predators and prey for each body, etc. -->


<!-- The basic parts of this model are nested: worlds contain bodies which contain brains. And brains are composed of both structure (which we think of as basically static) and activity (which we think of as basically dynamic).  For simplicity, we do not describe in detail the possible states of the world.  The relevant body states include, for example,  the position of each of its limbs.  The relevant states of brain structure include different morphologies, lesions, connectivities, etc.  And the relevant states of brain activity include whether each neuron is spiking or not, and the current protein expression level at each synapse.  The genome of an individual is another "part", although not in the same sense as the other parts: whereas each of which are physical entities, the genome is an abstraction.  The genome does not have any states to speak of for a given individual, rather, different genomic "states" correspond to different actual genomes, which are found in different individuals.  For the purposes of this model, this parts list is collectively exhaustive. In other words, parts that might not usually be thought of as "structure", such as the number of presynaptic vesicles in a given synapse, must be included in structure.  Similarly, parts that might not usually be thought of as "function", such as G-protein coupled expression patterns, must be included in activity.  That the line between structure and activity may be blurry at certain resolutions is not a problem in this model. -->

<!-- #### Causal Activities -->
<!-- i'd replace "motor" with "movement"  -->
<!-- i don't see the value of adding behavior? -->
<!-- genome should be a different color -->

<!-- 
There are three causal feedback loops governing the interactions of the parts of this model both within and across levels. Each causal process is characterized by the statistical regularities governing the likelihood of some parts' state due to another part's state.

1. **Brain**: Brain activity includes many things: spiking activity, gene expression, Dopamine release, etc. Brain activity can causally act on the brain, changing it (for example, as in activity dependent plasticity), or on the body, causing movements, heartbeats, swallowing, etc.
2. **Body**: Body activity includes movements, heartbeats, and swallowing, for example.  Those body activities that cause dynamics in the world are behaviors, those body activities that directly cause changes in the brain are sensations.
3. **World**: World activities include the sun setting, the leaf falling, and the tiger hunting.  The world activities that increase the chance of death lead to eliminate of certain behaviors, and those activities that decrease the chance of death survive to the next general.  This collective set of activities, in terms of its causal impact on bodies, is selective pressure.  -->


<!-- 4.  Brain structure  imposes biophysical statistical rules governing brain activity, and  brain activity can cause  changes brain structure via plasticity.  -->
<!-- 5.  Brain activity also causes body movements (and other changes of body state). Those body movements cause changes in the world's state.  Both kinds of changes of state--body  and world--are sensed by the body, and those sensation propagate to the brain and spinal cord, which can than cause further body/world changes.    -->
<!-- 6. The world--specifically the environmental niche in which a given animal resides--causes animal bodies to respond in various ways. For example, if a tiger enters an antelope's environment, it tends to run away.  The causal force at work here is selective pressure: antelope's have evolved to run from tigers. Those antelopes that tended to run away from tigers faster and better tended to survive, whereas the population of antelopes that tended to be eaten by tigers tended to be eliminated. Survival increases the antelope's chances at successfully procreating, which causes the creation of a new genome. Once a new genome is formed, development is the set of causal processes that leads to a new organism, with a brain and a body, and the cycle can repeat.  Specifically, the genome, via development, causes particular states of brain structure, as well as the details of activity dependent plasticity.  In other words, development is a causal process governing changes in brain structure over the lifetime of the individual.   The genome therefore does not directly cause any brain activity, or changes in brain activity. -->


<!-- #### Organization -->


<!-- The phenomenon of interest is a complex dynamical system.  This particular dynamical system operates at several different spatiotemporal scales: -->

<!-- - *Organization*:  -->
<!-- The above three causal loops are organized into nested spatiotemporal scales and various levels.  -->
<!-- 1. Brain activity  operates at second rates and subcellular resolutions.
2. Body activity operates at  minute rates and organ resolution.
3. World activity operates at lifetimes rates and whole body resolutions. -->
<!-- The causal processes governing activity are effectively at the level of statistical mechanics, where as the other causal processes operate at quite different levels.  Activity dependent plasticity, selective pressures, and development operate at different slower time-scales and coarser spatial scales, so statistical mechanical explanations are less appropriate.   -->
<!-- Note that each of these causal activities operates in loops, that is, brain activity impacts brains and bodies, body activity impacts body and world, and world activity impacts body and world.  However, these are not quite loops, because they do  not return to where they started, but rather start in a new (and hopefully improved) place, -->

<!-- In addition to the above scales, initial conditions are required for any dynamical system. In this case, rather than characterizing the initial conditions of the entire system, we just state the initial conditions for a new brain/body pair: its genome. In this model, the genome refers to the somatic genome of an individual, that is, the base-pair sequence of the first cell of that individual.  This genome provides the development plan, which is the blueprint for how the brain should develop and adapt. -->


<!-- #### Implications -->

<!-- The implications of the above conceptual model is that the primary mechanism by which an individual can give its procreation's guidelines by which they can thrive in a competitive environment, is via encoding a developmental program in its genome that results in brains that  impose biophysical constraints that yield movements that increase the probability of surviving and procreating.  In other words, **the brain  is the mechanism by which the genome can encode its preferred behaviors, that, when combined with the body (and physics) yields the desired behaviors with sufficiently high probability to help the organism win the evolutionary game its niche imposes on it.**  

Our perspective is that the above view of the role of brain structure is essentially dogma, though often implicit. Making it explicit justifies and motivates a serious modeling effort geared to understanding the relationship between the genome, brain structure, and behavior. -->