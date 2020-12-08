---
layout:     post
title:      "Why Statistic of Correlation Follows t-distribution?"
subtitle:   "A statistical derivation"
date:       2020-12-07
author:     "Yuhao Zhu"
header-img: "img/post_head_pic_js.jpg"
tags:
    - Statistics
---


# Introduction
We know that the statistic for the Pearson correlation coefficient follows the *t*-distribution with a degree of freedom of $n-2$. That is to say that $$n-2$$.

$$t=\frac{r}{\sqrt{1-r^2}}(n-2)\sim t_{n-2}.$$

Why?

# Derivation
## Assumptions
Assume that $(X, Y)$ follows a bivariate normal distribution with the parameters $(\mu_X, \mu_Y, \sigma_X, \sigma_Y, \rho)$.