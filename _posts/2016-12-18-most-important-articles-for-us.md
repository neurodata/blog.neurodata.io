---
layout: post
title: Useful Background Reading for NeuroData
description: ""
modified: 2016-12-18
category: misc
author: Joshua Vogelstein
tags: [publicity, collaboration]
imagefeature: to_the_cloud.jpg
comments: true
share: true
featured: true
---

In this post I highlight some of the most important books and articles for our group, and likely other groups. This list is certainly imperfect, so please comment about books/articles that you think are missing. 

### Books as references:

1. [exploratory data analysis (tukey)](https://www.amazon.com/Exploratory-Data-Analysis-John-Tukey/dp/0201076160)
1. [testing statistical hypotheses](https://www.amazon.com/Testing-Statistical-Hypotheses-Springer-Statistics-ebook/dp/B00DZ0O04O/ref=sr_1_1?s=books&ie=UTF8&qid=1482089959&sr=1-1&keywords=9780387276052)
1. [theory of point estimation](https://www.amazon.com/Theory-Point-Estimation-Springer-Statistics/dp/0387985026/ref=asap_bc?ie=UTF8)
1. [convex optimization (boyd & other dude)](https://www.amazon.com/Convex-Optimization-Stephen-Boyd/dp/0521833787/ref=sr_1_1?s=books&ie=UTF8&qid=1482090079&sr=1-1&keywords=convex+optimization)
1. [elements of information theory (cover & thomas)](https://www.amazon.com/Elements-Information-Theory-Telecommunications-Processing/dp/0471241954/ref=sr_1_1?s=books&ie=UTF8&qid=1482090107&sr=1-1&keywords=cover+and+thomas+information)
1. [elements of statistical learning (tibs & co)](http://statweb.stanford.edu/~tibs/ElemStatLearn/)
1. [robust statistics (huber)](https://www.amazon.com/Robust-Statistics-Peter-J-Huber/dp/0470129905)
1. [density estimation (silverman)](https://www.amazon.com/Density-Estimation-Statistics-Data-Analysis/dp/0412246201)
1. [storytelling with data](https://www.amazon.com/gp/product/1119002257?ie=UTF8&creativeASIN=1119002257&linkCode=xm2&tag=storytellingwithdata-20): Read this before making any publication quality figures
1. [writing science](https://www.amazon.com/Writing-Science-Papers-Proposals-Funded/dp/0199760241/ref=sr_1_1?s=books&ie=UTF8&qid=1482101630&sr=1-1&keywords=writing+science): Read this before trying to write a paper


### Statistics / pattern recognition / data science:

These articles are not the most cited articles, and are not necessarily the first on a topic. 
However, each does an excellent job making a specific point that I believe is important to remember when doing data science.

1. Model Based Clustering (Fraley & Rafterty, 2002): Explains the relationship between density estimation (via gaussian mixture modeling) and clustering. Still the best approach to cluster with medium-dimensional data, imho
7. Model selection is arbitrary (George & Foster; 2000): Demonstrates that all the different model selection criteria are in fact arbitrary special cases of a general prior with 2 parameters
3. Energy Statistics review (Rizzo & Szekely, 2016): Explains energy statistics that can perform a variety of tasks in high-dimensional data
4. Random Forest (Breiman, 2001): Introduced random forest practice and theory, still the best "black box" machine learning algorithm
5. GMRA (Allard, Chen, Maggioni; 2012): Introduces and explains relationships between dictionary learning and machine learning, with theory and implementation to boot
6. [MLE for Misspecified Models (White, 1982)](https://www.jstor.org/stable/1912526?seq=1#page_scan_tab_contents): Shows that MLE yields the minimum KL distance between the truth and the feasible region
7. [manifold learning is "just" kernel pca (Ham et al. 2004)](http://dl.acm.org/citation.cfm?id=1015417): Links several different important manifold learning techniques
10. [knn](http://projecteuclid.org/euclid.aos/1176343886): Proves k-nearest neighbor is universally consistent regression
8. [grazing goat starves in high-dimensions](http://www.jstor.org/stable/2686517?origin=JSTOR-pdf): Shows that our intuition in high-dimensions is way off
9. [approximate nearest neighbor review](http://ieeexplore.ieee.org/document/4031381/): Well-written discussion on the original [LSH paper](http://www.cs.princeton.edu/courses/archive/spring13/cos598C/Gionis.pdf) and subsequent work, demonstrating that randomization is a very useful approximation
1. [MSE doesn't work in >2 dimensions (Stein, 1960)](https://projecteuclid.org/euclid.bsmsp/1200501656): The geometric reason that sparsity and other forms of regularization can help in finite samples
1. [lasso doesn't work, even in true model](https://arxiv.org/abs/1511.01957): Shows that the lasso path includes lots of false positives, even when there are no correlations and the signal is sparse, and therefore shouldn't be trusted
1. [generalized linear models](http://projecteuclid.org/download/pdf_1/euclid.ss/1177013604): Showed that one can estimate many reasonable nonlinear regression functions with a sum of very simple nonlinear functions, though not used so much in practice these days, still a very important concept
1. [statistical pattern recognition (Jain, 2000)](http://ieeexplore.ieee.org/document/824819/): A wonderful review, shows the Trunk example that the optimal parameter/model with finite data is not necessarily the truth.
1. [imagenet classification via deep learning](https://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf): Shows that with lots of training data, flops, on images, deep learning dramatically outperformed previous methods
1. [Statistical modeling: The two cultures (with comments and a rejoinder by the author)](http://www.stat.uchicago.edu/~lekheng/courses/191f09/breiman.pdf) Explains the difference between machine learning and statistical modeling, but before the term "machine learning" was cool.
1. [Classifier Technology and the Illusion of Progress](https://arxiv.org/pdf/math/0606441.pdf). In particular, it cites Hoadley, "Hoadley, in the same discussion, “coined a phrase called the ‘ping-pong theorem.’ This theorem says that if we revealed to Professor Breiman the performance of our best model and gave him our data, then he could develop an algorithmic model using random forests, which would outperform our model. But if he revealed to us the performance of his model, then we could develop a segmented scorecard, which would outperform his model.”



### Other people's neurodata collection:

1. [Array Tomography](http://cshprotocols.cshlp.org/content/2010/11/pdb.top89.full.pdf+html) for collecting multispectral 3D gene expression maps, and [Knowing a synapse when you see one](http://journal.frontiersin.org/article/10.3389/fnana.2015.00100/full) for more discussion.
1. [CLARITY](http://www.nature.com/nmeth/journal/v10/n6/full/nmeth.2481.html) and [iDisco](http://www.cell.com/abstract/S0092-8674(14)01297-5): For seeing whole brains with fluorescence without physically sectioning
1. [Serial EM](http://www.nature.com/nature/journal/v471/n7337/abs/nature09802.html) For seeing large volumes of nanoscale neuroanatomy
1. [Multimodal MRI](http://www.nature.com/nmeth/journal/v10/n6/abs/nmeth.2482.html) For seeing in vivo non-invasive brain structure and function at millimeter scale
1. [Calcium imaging](http://www.nature.com/nmeth/journal/vaop/ncurrent/full/nmeth.3040.html) for seeing whole brain activity in zebrafish, or a whole bunch of activity in other stuff
1. [Behavior](http://science.sciencemag.org/content/344/6182/386.long) For characterizing "natural" behaviors and linking them to neurons.
1. [Biomarkers in psychiatry](https://www.researchgate.net/profile/Karen_Seymour2/publication/261507750_Consensus_Report_of_the_APA_Work_Group_on_Neuroimaging_Markers_of_Psychiatric_Disorders/links/0c9605346a4d865d9b000000.pdf) Stating that clinical psychiatrists do not yet utilize any brain imaging based biomarkers for any clinical diagnosis (as of july 2012).  

### Our work:

1. [Incommensurability phenomenon](http://link.springer.com/article/10.1007/s00357-016-9203-9): Shows that if you run PCA twice on two different samples of noisy data, you can get arbitrarily different results
1. [You say, I say](http://www.cis.jhu.edu/~parky/CEP-Publications/scgn-21-2.pdf): Shows that graph invariants are test statistics, and therefore, we can determine which invariants are optimal for any test by thinking about them in these terms
1. [Graph Matching: Relax at your own risk](http://ieeexplore.ieee.org/document/7091002/): Shows that we can use a convex analytic approximation to initialize a non-convex numerical approximation, and get good results on an NP-hard problem, even when the convex approximatino is probably bad
1. [Consistency of ASE](http://amstat.tandfonline.com/doi/abs/10.1080/01621459.2012.699795): Shows that spectral embedding yields consistent estimators of latent positions for random graph models, so then we can use them in typical machine learning algorithms for subsequent inference
1. [HSBM](http://ieeexplore.ieee.org/document/7769223/): One of the best statistical models of large graphs we know
1. [MGC](https://arxiv.org/abs/1609.05148): Shows that we can use and estimate locality for certain exploitation tasks, improving upon previous dependence tests both theoretically and empirically
1. [FlashGraph](https://arxiv.org/abs/1408.0500): Demonstrates the power of semi-external memory modeling to build algorithms on single-node multicore machines that best cluster implementations with orders of magnitude more resources
1. [Open Connectome paper](https://arxiv.org/abs/1306.3543): Explains the basis of our spatial database
1. [mi-lddmm](https://arxiv.org/abs/1612.00356): The current best approach for nonlinear registration, imho
