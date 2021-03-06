---
layout: post
author: Shekhar Jha
title: "Startup Crunchbase EDA"
excerpt_separator: <!--more-->
image: https://jhashekhar.github.io/assets/img/startup_p/funding_yoy.gif
date: 2020-07-05

github:
    is_project_page: true
    repository_url: "https://github.com/jhashekhar/startup-cb"
---
<title-head><h1>{{ page.title }}</h1></title-head>
<br>
<p>This is Part-1 of a series of two post where I will be trying to visualise and use machine learning algorithms to make predictions for the data.</p>

<p>
Below are the links to data and code:
<ul>
    <li><a href="https://www.kaggle.com/arindam235/startup-investments-crunchbase">Data</a></li>
    <li><a href="https://github.com/jhashekhar/startup-cb">Code</a></li>  
</ul></p>

<p>
This post is divided into three sections:
<ol>
<li>Motivation</li>
<li>Basic Data Cleaning</li>
    <ul>
        <li>Data</li>
        <li>Approach</li>
    </ul>
<li>Analysis</li>
</ol></p>


<h3> 1. Motivation </h3>

<p>Before getting into Data Science and ML I used to work at a firm where part of my job comprised of interactions with a lot of different clients who were mainly medium business enterprises, I always wondered are they going to remain profitable, will they grow or they will fail and be out of business(this wasn't part of my job, but my boss's job). 

<br><br>

So, when I started with Data Science and encountered on this dataset, I couldn't stop myself from using my newly learnt skills, to do exactly the same using algorithms for startups.
</p>

<h3> 2. Let's explore the data </h3>

<h4> 2.1 Data </h4>

<p>So, let's have a little peek into the data: there are 54294 startups with 39 different features in the dataset. The data consists of diverse features like categorical features - <b>status, market, country</b> etc. and numerical features - <b>funding_total_usd, seed, venture</b> etc. and other features - <b>founded_year, founded_month, permalink, region, category_list</b> etc. We will go into detail on most of the features in the below sections and analyze them accordingly.</p>

<h4> 2.2 Approach </h4>

<p>There are a lot of variables in the data. We can delve deeper into each of these but that would make the post long and hard to parse through. Instead, I will try to answer some important questions about the datasets in this post.</p>


<p>This post is structured around the following questions.
<ul>
    <li>How startups are distributed across different markets?</li>
    <li>Status, funding, categories of different startups?</li>
    <li>How much is the regional significance for the funding/growth of a startup?</li>
    <li>How funding is distributed across markets and categories?</li>
    <li>Are there outliers?</li>
</ul></p>

<h3> 3. Analysis </h3>

<p>My approach to analysis would be to answer some of the interesting questions. The questions are not in any specific order.</p>

<h3><i>How startups are distributed across different markets?</i></h3>

<p>We have a feature column <b>market</b>. Following is the barplot distribution of all startups across top ten markets with the number of startups operating, closed etc. till 2014.</p>


<img src="https://jhashekhar.github.io/assets/img/startup_p/bar_plot_1.png">

The markets

<p>Below the plot shows the percentages of startups across different markets.</p>

<img src="https://jhashekhar.github.io/assets/img/startup_p/piep-1.png">
<img src="https://jhashekhar.github.io/assets/img/startup_p/piep-2.png">

<h3><i>What role does region plays into funding and growth of startup? How region affects startups in terms of number and valuation?</i></h3>

<p>Is there an effect of region on markets or categories in which startups operate? How important is regional advantage? In our dataset we have two features that are relevant in finding the answer to this question. One is startup's country of origin and the other is state that is specific to USA.<p>

<p>Los Angeles is known for Hollywood/entertainment industry. New York is the finance capital of United States. So I want to inspect the effect of these uniqueness over the startup culture.<p>

<img src="">

<h3><i>How funding varies or distributed across markets and categories?</i></h3>

<p>One of the other point of interset is the funding of startup across market segments year over year.</p>

<!-- <img src="https://jhashekhar.github.io/assets/img/funding_across_market_segments.png"> -->
<img src="https://jhashekhar.github.io/assets/img/startup_p/funding_yoy.gif">

<!--
<h3><i>Are there outliers - in terms of fundings for various stages? Which market do they belong to?</i></h3>-->





