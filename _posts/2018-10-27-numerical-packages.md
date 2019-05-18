---
layout: post
title:  "11 Simple Rules for Releasing Data Science Tools"
date:   2018-10-21 14:27:57 -0400
tags:  [10, bits]
author: Joshua Vogelstein
---

These notes were co-written by myself and a number of other people, including [Greg Kiar](http://gkiar.me/), [Eric Bridgeford](http://ericwb.me/), [JB Poline](https://www.mcgill.ca/qls/researchers/jb-poline), and [Tristan Glatard](https://users.encs.concordia.ca/~tglatard/). Inspired by the FAIR Guiding Principles for scientific data management and stewardship (see [here](https://www.nature.com/articles/sdata201618)), we devised the FIRM guidelines for scientific software, specifically numerical packages.  The FIRM guidelines stipulate that anybody in the world should be able to: **F**ind, **I**nstall, **R**un, and **M**odify your code. Below is a working draft of our ideas; as always, your feedback is solicited. 


### Find

1. To make your code findable, we recommend three steps:
    1. Make the code open source on a searchable code repository (e.g., [github](https://github.com/) or [gitlab](https://about.gitlab.com/)).
    2.  Generate a permanent Digital Object Identifier (DOI) so that you can freely move the code to other web-servies if you so desire without breaking the links (e.g., using [zenodo](https://zenodo.org/)).
    3.  Add a license so that others can freely use your code without worrying about legal ramifications (see [here](https://opensource.org/licenses) for options).

### Install


1. Provide installation guidelines, including  *1-line installation* instructions with system requirements (including hardware and OS),  software dependencies, and expected install time.  

2. Deposit your code into a standard package manager, such as [CRAN](https://cran.r-project.org/) for R or [PyPi](https://pypi.org/) for Python. You might also provide a container or virtual machine image with your package pre-installed, for example, using [Docker](https://www.docker.com/), [Singularity](https://www.sylabs.io/docs/) or [Gigantum](https://gigantum.com/).


### Run

1. Provide a demo, including requisite data, expected results, and runtime on specified hardware. The demo should be simple, intuitive, and fast to run. We recommend using  [Rmarkdown](https://rmarkdown.rstudio.com/) for R and  a [Jupyter Notebook](http://jupyter.org/) for Python.

2. Write a readme with a quick start guide, including installation and a simplified (plain text) version of the demo.


3. Make sure each function includes auto-generated documentation. We recommend  [Roxygen](https://cran.r-project.org/web/packages/roxygen2/vignettes/roxygen2.html) for R and   [Sphinx](http://www.sphinx-doc.org/en/master/) for Python.


### Modify

1. Include contribution guidelines, including: 
    1. style guidelines ([Google's](https://google.github.io/styleguide/Rguide.xml) or [Hadley's](http://adv-r.had.co.nz/Style.html) for R, or [PEP8](https://www.python.org/dev/peps/pep-0008/) for Python)
    2. bug reports, 
    3. pull requests, and  
    4. feature additions.
2. Write unit tests for each function. Examples are [testthat](http://testthat.r-lib.org/) for R and [unittest](https://docs.python.org/3/library/unittest.html) for Python.
3.  Incorporate continuous integration, for example, using either  [TravisCI](https://travis-ci.org/) or  [CircleCI](https://circleci.com/).
4.  Add the following [badges](https://shields.io/#/) to your repo: 
    9.  DOI. 
    8.  license,  
    4.  stable release version so people know which release they are on (from package manager), 
    5.  [documentation](https://readthedocs.org/) to indicate that you generated documentation, 
    2.  [code quality](https://codeclimate.com/) to indicate that your code is written using modern best practices, 
    3.  [coverage](https://coveralls.io/) to indicate the extent to which you have written tests for your functions, 
    1.  [build status](https://www.docker.com/) to indicate whether the virtual machine that contains the latest version of your code is running, 
    6.  total number of downloads, 
 1.  Finally, benchmarks establishing current performance (using appropriate metrics) on standard problems, and better yet also comparing to other standard methods. Ideally, the code the generate the benchmark numbers are provided in [Jupyter notebooks](http://jupyter.org/) provided in your [Gigantum](https://gigantum.com/) project.


A few examples of numerical packages that we have released that satisfy all (or most of) these rules include:
- [graspy](https://github.com/neurodata/graspy)
- [mgc](https://github.com/neurodata/mgc)
- [Randomer Forest](https://github.com/neurodata/rerF/)
- [ndmg](https://github.com/neurodata/ndmg)
- [LOL](https://github.com/neurodata/LOL)
- [ndreg](https://github.com/neurodata/ndreg)
