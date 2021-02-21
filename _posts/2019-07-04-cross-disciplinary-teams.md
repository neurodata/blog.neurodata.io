---
layout: post
title:  "Some thoughts on building interdisciplinary biological/data science teams"
date:   2019-02-10 14:27:57 -0400
tags:  [collaboration]
author: Joshua Vogelstein, Danilo Bzdok
---

I recently was asked a few questions on this topic, and thought I'd share my answers.  I did, tweeted it, and then updated this post based on public and private responses.  For the twitter discussion, including contributors, please see [here](https://twitter.com/neuro_data/status/1146830916863631361).  I'm grateful to everyone who has contributed to this dialog. If anybody has contrary opinions, I'd love to know about them.

What do effective biologist/data scientist teams look like?

While I'm sure there are many different flavors of succesful teams, *we* have been most succesful when team  have the following properties:

1. A relatively concrete biological question, with a careful experimental design.  Good data scientists can find patterns in anything, but not all patterns are scientifically interesting.  
2. The data scientist is integrated into the scientific process as early as possible.  For example, there are often choices the experimentalist could make that would result in much easier or more difficult challenges for the data scientist. Only by virtue of the data scientist being engaged before the data are collected is it even possible for them to provide input into these decisions.  
3. Both the data scientist and the neurobiologist have deep respect for the other's time and expertise. In particular, both realize that the challenges the other faces are difficult to overcome, and may take time.  At the same time, both realize that they are working to answer a particular question, rather than solve some "generic" problem.  For example, the data scientist must develop an algorithm that detects cell bodies with sufficiently high sensitivity and specificity to answer the particular neurobiological question of interest, rather than "the best cell body detection method ever".  This may require either or both individuals to go outside their comfort zones at time for the success of the project. 
4. If novelty and complexity are not required for the methods, even if such properties would be sexy, neither party insists on pursuing such approaches, which can be quite time consuming and typically not a dramatic improvement on existing technology. 
5. Often making authorship agreements up front can avoid future clashes.  One workable approach is a single manuscript approach, with  first-author and corresponding-author rights shared by both labs.  Another reasonable approach is a two-manuscipt approach, with one manuscript describing the data science technique, and another describing the biology.  A potential downside to this approach is that often the data science technique does not have a natural "peer reviewed" home, because it is a "trivial" extension of previous work. That is not to say that it did not require a Herculean amount of work to get it working sufficiently well, but rather, that many stats/AI/ML peer-reviewed venues do not highly value this kind of work.
6. Each team member should be able to go out of one’s comfort zone to admit and know what he/she does not (yet) know  


One caveat to the above, is that it assumed a legitimate collaboration.  Sometimes, the biologists simply needs a consultant, to check their work, suggest a complementary strategy, etc.  Those can often be quite fruitful for the biologist, although the data scientist rarely gets any "academic credit" for such efforts.  On the other hand, for serious collaborations, getting the data scientist up to speed on the biology can often take quite some time, for example one to two years even.  Doing so is a considerable energetic investment for all parties involved.  In these cases, it can be advantageious for everyone if there are smaller "wins" in the interm period that indicate to all parties that continued investment is likely worthwhile. 


 
How deeply are they integrated?
 
In our experience, weekly (potentially remote) meetings between both neurobiologist and data scientist are incredibly helpful to discuss current results and get further direction for next steps.  The data scientist also visits the neurobiologist at least once in the beginning of the project to witness a day of experiment, to understand what the data are.  Quarterly or semi-annual in person visits are also quite beneficial, in our experience. 

What is the management structure?

Usually one trainee acquiring data and one trainee developing/applying methods, each supervised by their respective PI.  Once the method is fairly well established and routinely able to run by the data science trainee, it is often helpful to engage a software engineer on the data science side, to transition the code from "gradware" to at least "labware", meaning that other people in the data science lab could also run the analysis, thereby freeing up the trainee to write a manuscript, further develop the method, or transition to other projects.  Another complementary option is to engage a younger trainee to transition the project to them.  

 
Do you have a sense for if the data scientists in the teams will continue in tackling tough biological problems, or is this perceived more as a training opportunity for junior researchers/scientist who may be looking at industry careers?

With the artificial intelligence industry sky rocketing, a large fraction of trainees are interested in transitioning to industry.  Industry can be start-ups, big tech companies, the financial sector, or biotech. In each of those industries, there are now opportunities to work in data science as applied to biological problems, particularly in healthcare.  Those trainees that are motivated specifically to tackle the biology question are more likely to continue doing so when they graduate.  And in fact, those that are inspired to actually solve the problem, rather than transition to a different industry, I find to be much more effective at solving the biological question.   

