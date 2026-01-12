---
layout: page
title: Parallelizing Bayesian Trees - Algorithmic Insights from GPU BART
description: Somewhat of WIP
img: assets/img/bartpicture.png
importance: 2
category: fun
giscus_comments: false
---

Abstract: In the past decades, many algorithms have been modified to run on Graphics Processing Units (GPUs) to utilize increased processing power. Neural networks and convolutional networks are some prominent examples. These changes have occurred due to the development of new plat- forms, such as Compute Unified Device Architecture (CUDA), which supports optimized libraries for low-level matrix computations like cuBLAS, which enables the development of high-level frameworks such as JAX. This has spurred the development of branchless and parallelizable versions of preexisting algorithms. BART (Bayesian Additive Regression Trees) is a sum of tree methods released in 2010 which has been frequently used for non-parametric estimation due to inference proficiency. The literature around BART algorithm has expanded greatly within the prior decade with many implementations focused on accelerated computing. BARTZ, also referred to as GPU-BART (Super-Fast Bayesian Additive Regression Trees) is one recent addition, which utilizes GPU computation, enabling speed-ups of an order of magnitude on large datasets. We at- tempt to both analyze and rigorously stress-test BARTZ to determine whether modifications are extendable to the domain of causal inference. After rigorous testing, BARTZ matches the perfor- mance of commonly used libraries for nearly all surfaces, only struggling with a few theoretical surfaces and edge cases.

<div style="text-align: center;" markdown="1">

<a href="/assets/pdf/example_pdf.pdf" target="_blank" class="btn btn-lg z-depth-0" role="button">Download PDF</a>

</div>
