---
author: Aidan Gildea, Jenny Huang, Bella Larsen, Jessie Bierschenk
categories:
- Data Science
- R Shiny
- Regression Analysis
date: "2020-11-7"
draft: false
layout: single
links:
- icon: github
  icon_pack: fab
  name: code
  url: https://github.com/sta210-fa20/project-approximately-normal
subtitle: STA 210 - Regression Analysis
tags:
- hugo-site
title: Voter Turnout Data Analysis
---

### About this Project

In this project, we investigated voter turnout rates over a 14-year period. We used data from IPUMS and the American Statistical Association that that were originally collected from surveys conducted by the United States Census Bureau and the Bureau of Labor Statistics [1,2]. The surveys are part of a “Voting and Registration Supplement” of the Current Population Survey that occurs every two years after the November elections [3]. We used logistic regression and model selection processes (backward selection using AIC and drop-in-deviance tests) to predict whether a person voted or not based on predictor variables including sex, age, marital status, veteran status, citizenship status (native born or naturalized citizen), whether or not someone is Hispanic or Latinx, employment status and more. We assumed a hypothetical role of an organization planning to distribute mailers to encourage people to vote, with the goal of minimizing wasted resources by only sending mailers to the people who are not likely to vote using a decision threshold based on our final model.

This analysis's code can be found on [Github](https://github.com/sta210-fa20/project-approximately-normal).


References:
[1] The University of Minnesota. “What Is IPUMS?” Text. IPUMS, February 7, 2019. https://ipums.org/what-is-ipums.
[2] American Statistical Association. “Fall Data Challenge: Get Out the Vote!” This Is Statistics. Accessed November 17, 2020. https://thisisstatistics.org/falldatachallenge/.
[3] American Statistical Association. “ASA’s 2020 Fall Data Challenge: Get Out the Vote! Challenge Dataset FAQ,” n.d. https://thisisstatistics.org/wp-content/uploads/2020/09/2020-Fall-Data-Challenge-DatasetFAQ-PDF.pdf.
