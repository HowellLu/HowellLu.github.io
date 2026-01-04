---
layout: page
title: My Relationship Future
description: A Website
img: assets/img/myrelationshipfut.png
importance: 3
category: fun
---

This work is an extension of the paper “History Matters”, it extends the methodology of Finite Mixture Models onto the NSLY79 dataset rather than the Swiss Dataset. It attempts to predict a future timeline for individuals when given a sequence of life events, gender and a childhood rearing situation (Single-Parent, Dual-parent and etc). 

Finite Mixture Models allow for a regression to be split into multiple components which are applied to sub-populations for different outcomes on regression. For example, weight ~ height + income + education, k = 2 might split into two components. One component might apply to highly educated sub-populations which don’t see an increase in weight with high income. The second component could be a low education subpopulation with an no association between weight and income. However, our real outcome variable is the relationship status of an individual (we use multiclass logistic regression) and we utilize 11 different components. The website calculates posterior probabilities on the given subsequence from users to classify users into a component and then computes the regression to extrapolate a future timeline. 

<div style="text-align: center;" markdown="1">

<a href="https://www.myrelationshipfuture.com" target="_blank" class="btn btn-lg z-depth-0" role="button">Check out the website</a>

</div>
