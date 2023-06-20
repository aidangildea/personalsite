---
author: Aidan Gildea, Chandler Naylon, Marcus Liaw
categories:
- Data Science
- Data Analysis
- Classification
date: "2023-02-23"
draft: false
layout: single
links:
- icon: github
  icon_pack: fab
  name: code
  url: https://github.com/STA440-SP2023/case2-team12
subtitle: STA 440 - Case Studies
tags:
- hugo-site
title: Classifying DNA Barcodes from the Lepidoptera Orde
---

## About

As part of the course STA 440: Case Studies, we built classification models that read DNA sequences from various Lepidoptera (butterflies) to accurately predict their families and genera, while acknowledging any measured uncertainty. This case study utilized a historical dataset of 40,000 error-free annotated DNA sequences to fit and train our models, with the ultimate goal of classifying 7,000 unannotated sequences at the family and genus levels. We ultimately achieved a high level of accuracy by constructing a multinomial regression model accounting for particular loci (formally know as kmers) in the DNA sequences. 

You can view the project code on [Github](https://github.com/STA440-SP2023/case2-team12).