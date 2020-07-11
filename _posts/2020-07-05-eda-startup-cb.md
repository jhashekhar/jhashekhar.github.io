---
layout: default
author: Shekhar Jha
title: "Startup Crunchbase EDA - Part 1"
excerpt_separator: <!--more-->
date: 2020-07-05
---


This is Part-1 of a series of two post where I will be trying to visualise and use machine learning algorithms to make predictions for the data.  <!--more-->

Below are the links to data and code:

- [Data](https://www.kaggle.com/arindam235/startup-investments-crunchbase)
- [Code](https://github.com/jhashekhar/startup-cb)
- [Part 2](https://jhashekhar.github.io/2020-06-07-startup-cb-part2.md)
- [Part 3](https://jhashekhar.github.io/2020-07-07-startup-cb-part3.md)


This post is divided into three sections:
1. Motivation

2. Basic Data Cleaning
    - Data
    - Approach
3. Analysis

## 1. Motivation

Before getting into Data Science and ML I used to work at a firm where part of my job comprised of interactions with a lot of different clients who were mainly medium business enterprises, I always wondered are they going to remain profitable, will they grow or they will fail and be out of business(this wasn't part of my job, but my boss's job). 

So, when I started with Data Science and encountered on this dataset, I couldn't stop myself from using my newly learnt skills, to do exactly the same using algorithms for startups.

## 2. Basic EDA

### 2.1  Data

So, let's have a small peek into the data: there are 54294 startups with 39 different features about them in the dataset. The data consists of diverse features like categorical features **status, market, country** etc. and numerical features like **funding_total_usd, seed, venture** etc. and other features like **founded_year, founded_month, permalink, region, category_list** etc. We will go into details on most of the features in below sections and analyse them accordingly.

### 2.2  Approach

There are a lot of variables in the data. We can delve deeper into each of them but it will make the post very dense and hard to parse through. So instead I will focus the post around these questions, and then we can look for answers in the data.

This post is structured around the following questions.

- How startups are distributed across different markets?
- Status, funding, categories of different startups?
- How much is the regional significance for the funding/growth of the startup? Which region has more startups?
- How funding varies or distributed across markets and categories?
- Are there outliers - in terms of fundings for various stages? Which market do they belong to? 


## 3. Analysis

My approach to analysis would be to answer some of the interesting questions. The questions are not in any specific order.


## *How startups are distributed across different markets?*

We have a feature column **market**. Following is the barplot distribution of startups across top ten markets with the number of startups operating, closed etc.

![status of top 10 startups](https://jhashekhar.github.io/assets/img/bar_plot_1.png)

Below is the pie-chart showing the percentages of startups with their in differnt markets.

![status of top 4 startups](https://jhashekhar.github.io/assets/img/pie_plot_1.png)

## *What role does region plays into funding and growth of startup? How region affects startups in terms of number and valuation?*

Is there an effect of region on markets or categories in which startups operate? How important is regional advantage? In our dataset we have two features that are relevant in finding the answer to this question. One is startup's country of origin and the other is state that is specific to USA. 

Los Angeles is known for Hollywood/entertainment industry. New York is the finance capital of United States. So I want to inspect the effect of these uniqueness over the startup culture.

We will analyse all the cases.


## *How funding varies or distributed across markets and categories?*

Some startups are popular due to market they operate in for example, Uber, Yelp, Stripe are famous because they serve millions of coustomers every day, whereas there are startups that provide enterprise solutions, or they are operating in markets like BioTech, Medicine. So, are the ecommerce companies more.....


## *Are there outliers - in terms of fundings for various stages? Which market do they belong to?*





