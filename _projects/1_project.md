---
layout: page
title: Analyzing Life Outcomes Utilizing CFDA within a Survival Analysis Framework
description: with background image
img: assets/img/CFDAImage.png
importance: 1
category: fun
related_publications: false
pdf: assets/pdf/example_pdf.pdf
---

Abstract: We extend the usage of Categorical Functional Data Analysis (CFDA) onto the biofam dataset utilizing a Discrete-Time Hazards Model onto past sequence history data at differing periods along an individual’s lifespan to predict a terminal outcome within the next time state. To enable CFDA onto different sequences lengths within a hazard dataset, we normalize sequence lengths using trajectory’s relative duration. In addition, CFDA is compared against traditional methods such as Distinct Successive States (DSS) with Partition around Medoids (PAM) and a regression of the outcome variable against all distinct state sequences at given times.


This project attempted worked on the problem of capturing specific variation within sequence data on the biofam dataset to predict outcome events. Specifically, we utilized the data of 2,000 Swiss individuals to predict whether they would have been fully settled (Left Home, Married and Had Children) in the next year.  

One cannot utilize every possible sequence as that would lead to sparsity and overfitting, so there needs to be some way to compress the pathway of potential sequences into another dimensional space. We essentially utilize three different methods to attempt to capture an individual's sequence history: 

1.) Using an individual's person-period distinct state history as a predictor.

2.) Using PAM (Partitioning Around Medoids) on the Distance Matrix of DSS (Distinct Successive States), to create clusters to utilize as a predictor. 

3.) Using CFDA (Categorical Functional Data Analysis) on every individual's person-period state and normalizing each sequence to be of the same length and utilizing the CFDA principal components as predictors. 

CFDA on Normalized Sequences performed the best out of all 3 experiments and was able to partially capture some of the variation within distinct sequences. For example, someone who lived with their parents for 8 years and then lived alone for two would be different than one who lived with their parents for 2 years and alone for 8. This variation that would be captured with CFDA Principal Components and can be utilized for prediction, thereby yielding better estimates. 
<div align="center">

| Model | Training AIC | Testing AUC |
|:---|---:|---:|
| Regression on DSS | 5,180 | 0.8202 |
| Regression on PAM on LCS on DSS | 5,170 | 0.8209 |
| Regression on CFDA FPCs | 5,026 | 0.8375 |

</div>

<div align="center">

<a href="/assets/pdf/example_pdf.pdf" target="_blank" class="btn btn-sm z-depth-0" role="button">Download PDF</a>

</div>
