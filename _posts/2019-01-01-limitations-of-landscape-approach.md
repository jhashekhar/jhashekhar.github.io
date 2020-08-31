---
layout: post
author: Shekhar Jha
title: "Limitations of Landscape Approach for understanding Optimization"
tags: [deep learning, optimization, loss-surface, gradient-descent]
excerpt_separator: <!--more-->
date: 2019-01-01
---
<title-head><h1>{{ page.title }}</h1></title-head>
<br>
Here I will write briefly about different approaches towards convergence analysis in the case of Deep Neural Networks(DNN).

The first approach that has been taken by most researchers is the analysis of loss surface(landscape). The problem with
this approach is that the loss surface is multi-dimensional(millions of parameters) and we cannot visualize greater than
3 dimensional surface.

Another problem is the introduction of non-linearity in DNN. It's very hard to understand the effect of non-linearity over such an
over-parametrized setting.

As it has been pointed out in Arora et al. 2019 that loss surface analysis has two main conditions that should be met for convergence.

_First, no poor local minima - local minimum is as good as global minimum._

_Second, strict saddle property - the hessian has at least one negative eigenvalue for critical points other than the local minimum._

There is at least one direction along which the curvature is negative and that is required for us to escape saddle points.

Both of the above mentioned conditions that are considered to be sufficient to have convergence to global minimum are proved to not hold by different papers.

So we need to take a step back and look out for other approaches that could help us better understand optimization.
