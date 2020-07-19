---
layout: index
title: Shekhar Jha
description: Home page
---
<style>
#menu img {
    display: block;
    width: 100%;
    height: 100%;
  }
</style>

<title-head><h1 text-align="center">{{ page.title }}</h1></title-head>
<br/>
<p>Hi. I'm Shekhar. I'm enjoy working on topics related to Natural Language Processing, Generative Models and Computer Vision. Recently I've been experimenting a lot with various NLP tasks like Multlingual Learning, text summarization etc. and application of generative models in NLP.<br/><br/>

I've created <a href="https://github.com/jhashekhar/jigsaw-multilingual"> Multi-lingual Classification</a> model trained using TPUs in PyTorch. Performed<a href="https://github.com/jhashekhar/disaster-clf"> Disaster Classification </a> on tweet dataset.<br/><br/></p>

<p> You can read my blog<a href="blog.html"> here.</a></p><br/>

<p>Other links: <a href="https://github.com/jhashekhar"> Github  </a> / <a href="https://linkedin.com/in/jhas"> Linkedin </a> / <a href="https://kaggle.com/xanthate"> Kaggle</a> / <a href="blog.html"> Blog </a></p>

<!--
<h3>Recent Posts</h3>

{% for post in site.posts limit:2 %}
<table id="menu">
  <tr>
    <td width="180px" height="160px"><img src="{{ post.image }}"></td>
    <td><p><a href="{{ post.url }}"> {{ post.title }} </a> | {{ post.date | date: "%b %d, %Y" }} <br/>
    {{ post.content | strip_html | truncatewords: 40 }}
    </p></td>
  </tr>
</table>
{% endfor %}
-->