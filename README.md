# GPTID
Official code repository for article Intrinsic Dimension Estimation for Robust Detection of AI-Generated Texts. 

<i> We apologize --- it is under construction, for now. </i>

Text of the paper is available at <a href="https://arxiv.org/abs/2306.04723">ArXiv:2306.04273</a> .

## Introduction

Rapidly increasing quality of AI-generated content makes it difficult to distinguish between human and AI-generated texts, which may lead to undesirable consequences for society. Therefore, it becomes increasingly important to study the properties of human texts that are invariant over text domains and various proficiency of human writers, can be easily calculated for any language, and can robustly separate natural and AI-generated texts regardless of the generation model and sampling method. In this work, we propose such an invariant of human texts, namely the intrinsic dimensionality of the manifold underlying the set of embeddings of a given text sample. We show that the average intrinsic dimensionality of fluent texts in natural language is hovering around the value 9 for several alphabet-based languages and around 7 for Chinese, while the average intrinsic dimensionality of AI-generated texts for each language is ≈1.5 lower, with a clear statistical separation between human-generated and AI-generated distributions. This property allows us to build a score-based artificial text detector. The proposed detector's accuracy is stable over text domains, generator models, and human writer proficiency levels, outperforming SOTA detectors in model-agnostic and cross-domain scenarios by a significant margin. 

## How to use our code

Computing the text Intrinsic Dimension is a relatively straight process; however there are several different estimators based on ideas from different areas of mathematics and different assumptions on data structure. In our work we explored two estimators --- Maximum Likelihood Estimator (provided in <a href="https://scikit-dimension.readthedocs.io/en/latest/index.html#">scikit-dimensions</a> package).

File `IntrinsicDim.py' contains class performing <b>P</b>ersistence <b>H</b>omology based Intrinsic <b>D</b>imension (PHD) estimation.

## Requirements

Required packages:
- For PHD estimator:
  - NumPy
  - SciPy

- For MLE estimator:
  - Scikit-dimensions
  
- For language models:
  - Torch
  - Transformers

- Auxillary functions for the example in the notebook:
  - Pandas
  - Sklearn
  - Tqdm
