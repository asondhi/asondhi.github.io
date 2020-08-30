---
#layout: archive
title: ""
permalink: /research/
author_profile: true
---

# Counterfactual policy evaluation with balancing weights

![Bandit](/images/bandit.png)

<img align="right" src="/images/bandit.png">

In contextual bandit problems, actions are taken in response to some observed state in order to optimize a reward. Applications can be found in medicine, where personalized treatments are designed based on known patient history, and internet marketing, where advertisements can be tailored to user interests. The state-to-action mapping is known as a /policy/. In many practical applications, online learning is infeasible and practitioners must rely on off-policy evaluation (OPE) of logged data collected from prior policies. While recent work has made significant advances in using importance sampling for OPE, less attention has been paid to improving the quality of the importance weights themselves. 

In this work we present balancing off-policy evaluation (B-OPE), a simple procedure that directly optimizes for balance and can be plugged into any OPE estimator that uses importance sampling. B-OPE directly estimates the importance sampling ratio via a classifier which attempts to distinguish state-action pairs from an observed versus a proposed policy. B-OPE can be applied to continuous, mixed, and multi-valued action spaces without modification and is easily scalable to many observations.

A paper based on this work was published in the proceedings of the 2020 AISTATS conference.

[[Conference paper]](http://proceedings.mlr.press/v108/sondhi20a.html)    [[arXiv]](https://arxiv.org/abs/1906.03694)

# High-dimensional estimation and inference with two-way network structure

Penalization is widely used to fit regression models when the number of predictors is larger than the number of observations in the data set. Intuitively, this "shrinks" the dimensionality of the predictor space to make a model identifiable. Network-based penalties can be used to incorporate known information on dependencies between predictors. For example, given a gene expression network, the model can be fit such that connected genes have similar fitted coefficients. Likewise, penalties can also be used to account for known dependency structures among the observation units.  

We develop a penalized regression framework to analyze high-dimensional two-way network structured data using generalized linear models. Our method unifies the incorporation of feature and unit network information in the high-dimensional setting, and also provides a statistical inference procedure for testing the individual association between the outcome of interest and a feature in the model. An application to a real-world metabolomics profiling study suggests that our model can improve classification of diseased subjects, and select relevant metabolites more often than standard methods.

An R package implementing this method is available on GitHub, and a paper based on this work is currently under review. A preprint is available on request.

[R library](https://github.com/asondhi/glmfunk)

# Learning causal networks from observational data

Directed acyclic graphs (DAGs) are used to represent causal relationships between a set of random variables. For example, in gene regulatory networks, directed edges represent regulatory interactions among genes, which are represented as nodes of the graph. Because experiments can be costly to run, especially in the high-dimensional setting, it is of interest to estimate DAGs from observational data. These can then be used to generate causal hypotheses and design more efficient experiments. 

We propose a new algorithm for estimating DAGs, which is a modified version of the well-known PC-Algorithm. Our proposed method offers significant gains in both computational complexity and estimation accuracy, particularly for graphs with hub nodes. We develop the theory for our algorithm by directly incorporating properties of random graph models. As a result, our method also requires less stringent assumptions for consistency than the PC-Algorithm. 

A paper based on this work was published at the Journal of Machine Learning Research, and an earlier version was published in the proceedings of the 2016 IEEE DSAA conference.

[Journal paper](http://jmlr.org/papers/v20/17-601.html) | [arXiv](https://arxiv.org/abs/1806.06209) | [Conference paper](http://ieeexplore.ieee.org/abstract/document/7796967/)

# Association testing for rare genetic variants

In genome-wide association studies, researchers test for associations between having a particular genetic variant and having a disease or other phenotypic outcome of interest. Using case-control data, relevant statistical tests are well-studied. However, when a genetic variant is rare in the sample, standard tests do not properly control the Type I error rate at the nominal levels required in these studies.

In this work, we consider improved permutation-style tests which can be computed relatively quickly for genome-wide data. Using analytical calculations, we show these tests outperform standard methods in the rare variant setting. We also find the results are sensible when applied to a real data set.

A paper based on this work has been published at the Annals of Human Genetics, and an R package implementing these tests is available on CRAN.

[Journal paper](https://doi.org/10.1111/ahg.12229) | [arXiv](https://arxiv.org/abs/1712.06643) | [R library](https://cran.r-project.org/package=AUtests)

