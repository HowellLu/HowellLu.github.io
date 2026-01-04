---
layout: page
title: Is My Degree Worth It?
description: A Website
img: assets/img/imdwi.jpg
importance: 4
category: fun
---

What is the economic value of a college degree and how does it differ for different individuals? This website attempts to solve this and was inspired by the paper: “Is College Worth It” by Douglas A. Webber. It required three components:

1.)	The calculation of an individual’s lifetime earnings in their original timeline. This is generated using the real-life salaries of those who had graduated from specific programs utilizing data from the College Scorecard and the American Community Survey (AVS).

2.)	The calculation of an individual’s counter-factual timeline. This is the calculation of how much the individual would have made if they had decided not to go to college, given their specific career choices, using the American Community Survey salary figures. 

3.)	Modifications to the timeline to account for individual traits. I calculated modifications for the lifetime earnings of an individual who did not go to college using a Random Forest estimator. It was trained on the NLSY79 dataset and it computed the Ratio of: Individual’s Salary while Controlling for all given individual attributes / The Individual’s Salary while only controlling for a career path. This ratio would be applied to the calculation of an individual’s lifetime earnings without a college degree.

In retrospect, quite a bit could have been improved. There is a lot of poorly modelled heterogeneity and quite a lot of unmeasured heterogeneity among other issues. Here are some of the most obvious ones which spring to mind. 

1.)	Transportability issues with time delays:  This is a pretty large issue given that the NLSY79 cohort was going to college in the late 90s, but the College Scorecard creates projections starting from the current day. Income projections and even personality measures may have changed in the last 20 years. 
2.)	Lack of data: There just isn’t enough data within the NLSY79 to account for all career trajectories, thereby we cannot capture that heterogeneity. Narcissism would increase the earnings of an actor significantly, but would not significantly impact or reduce the salary of an Air Traffic Controller. 
3.)	Poor data collection: Just generally something which frequently occurs in the ACS. There would often be physicians with only a high school degree and construction workers who were over 100 years old. I removed the most egregious abnormalities, but the data is not very clean.  
4.)	Did not use non-parametric statistical techniques and I did not model the parameters: I utilized a regression with second order interactions, simply because the American Community Survey was as over 3 million rows. However, I should’ve definitely used something closer to BART (Bayesian Additive Regression Trees) and dealt with the computational training demands by using cloud compute. 
5.)	No adjustment for the lifetime earnings of the individual if they go to college: It felt as if there simply wasn’t data to make that computation because of the amount of sparsity within the NSLY79 dataset. Let’s assume that a user wishes to calculate the difference that extreme grittiness makes for an MIT educated mathematics major. The NLSY79 would not have a parameter that measures highly selective colleges nor would it have sufficient data to infer what type of effect grit would make for this specific college path. I likely would need to use another data source.


I feel the most strongly about this project out of the all of the other ones because I believe this was the most ambitious question I've worked on and I used a series of kludges to make it all work. If I were to return to this, I would use much better statistical models and have designed it a very different way. 

Here is the website: 

<div style="text-align: center;" markdown="1">

<a href="https://www.ismydegreeworthit.com" target="_blank" class="btn btn-lg z-depth-0" role="button">Check out the website</a>

</div>

