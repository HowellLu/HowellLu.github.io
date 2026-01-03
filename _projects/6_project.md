---
layout: page
title: project 6
description: a project with no image
img:
importance: 6
category: fun
---

This was a former interview question on a given dataset: Presume that I am a firm which disburses loans to individuals and I am unable to discriminate on the individual level. I wish to find a ruleset on the which generates the largest profit. You are given a dataset of historical loans and asked to create a ruleset which would create the largest net profit.  

I proposed a genetic algorithm. The first step would be to throw out random points in n-dimensional space and randomly generate partitions around these points. The partition which returned the highest objective values would be retained and then an sequence of stochastic gradient descent would be run on the boundaries of these partitions followed by occasional genetic mutation on the operators of the partition, replacing the current partition if objective value is higher.  After a select number of iterations, the code would sample the dataset again, thus generating points in n-dimensional space again and calculate whether the partitions capture more of the objective function compared to the current best partitions. If the new partitions dominate over the present best partitions, the new partitions take the place of the former partitions and stochastic gradient descent is run of the boundaries of those partitions.

<a href="https://www.yahoo.com" class="btn-standard" target="_blank" rel="noopener noreferrer">
  See My Work
</a>

<style>
.btn-standard {
  background-color: #222;
  color: white;
  padding: 10px 20px;
  text-decoration: none;
  border-radius: 5px;
  font-family: sans-serif;
  font-weight: 500;
  display: inline-block; /* Check out the library */
}

.btn-standard:hover {
  background-color: #555;
}
</style>
