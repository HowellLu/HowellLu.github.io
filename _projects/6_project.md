---
layout: page
title: project 6
description: a project with no image
img:
importance: 6
category: fun
---

This was a former interview question on a given dataset: Presume that I am a firm which disburses loans to individuals and I am unable to discriminate on the individual level. I wish to find a ruleset on the which generates the largest profit. You are given a dataset of historical loans and asked to create a ruleset which would create the largest net profit.  

I proposed a genetic algorithm. The first step would be to throw out random points in n-dimensional space and randomly generate partitions around these points. The partition which returned the highest objective values would be retained and then stochastic gradient descent would be run on the boundaries of these partitions followed by occasional genetic mutation on the operators of the partition, replacing the current partition if objective value is higher.  After a select number of iterations, the code would sample the dataset by generating points in n-dimensional space again and calculating whether these new paritions dominate the existing best split. If the new partitions dominate, then stochastic gradient descent and the occasional genetic mutation is run on the boundaries of the new partition instead of the current one. This is run for a fixed number of iterations.

Given that I haven't really quite seen an easy plug and play library that did this, I created a python library for this method. The link is below.


<div style="text-align: center;" markdown="1">

<a href="https://pypi.org/project/simplyincluded/" target="_blank" class="btn btn-lg z-depth-0" role="button">Check out the Library</a>

</div>
