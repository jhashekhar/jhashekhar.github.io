---
layout: post
author: Shekhar Jha
title: "Diffusion Limited Aggregation"
image: "https://jhashekhar.github.io/assets/img/diffusion_p/n_200_k_1000_1.gif"
excerpt_separator: <!--more-->
date: 2020-01-20
---
<title-head><h1>{{ page.title }}</h1></title-head>
<br>

<p>In one of my job application process I received an assignment related to Diffusion Limited Aggregation. At that time I somehow managed to do part of the assigment. But got overwhelmed by it and gave up. A couple of days ago, I thought to give it another shot. So here are initial results.</p>

<p>I'm using python, matplotlib, seaborn, gif libraries to generate the visuals.</p>

<p>The visualization generating processing is quite long. It takes hours to generate cool visuals, more on this later. So sharing visuals in this post would be ongoing process. Right now I'm sharing some of my inital results and observations.</p>

<p><b>Reference: </b><a href="http://paulbourke.net/fractals/dla/"> Diffusion Limited Aggregation</a>. Please read this linked post. Apart from 2 dimensional DLA they also talk about 3 dimensional DLA and how that can render cool visualization of natural processes.</p>

<p>Below is the DLA progression known as Point Attractor for N = 100, N = 1000, N = 2000, where N is the number of particles.</p>

<table style="width: 100%; text-align: center;">
<tr>
    <td><img src="https://jhashekhar.github.io/assets/img/diffusion_p/n_200_k_100.gif"></td>
    <td><img src="https://jhashekhar.github.io/assets/img/diffusion_p/n_200_k_1000_1.gif"></td>
    <td><img src="https://jhashekhar.github.io/assets/img/diffusion_p/n_200_k_2000.gif"></td>
</tr>

<tr>
    <td>N = 100</td>
    <td>N = 1000</td>
    <td>N = 2000</td>
</tr>
</table>

<!--<img src="https://jhashekhar.github.io/assets/img/diffusion_p/n_500.png" width="400px" height="400px" align="center">-->
