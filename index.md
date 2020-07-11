---
layout: index
title: Shekhar Jha
description: Home page
---
<h1 text-align="left">{{ page.title }}</h1>
<p>Hi, I'm currently in the process of transitioning to Machine Learning field from Consultancy. I'm interested in NLP, Meta Learning, Optimization and Computer Vision.<br/><br/>

Few of my projects are<a href="https://github.com/jhashekhar/jigsaw-multilingual"> Jigsaw Multilingual </a> using TPUs and PyTorch, <a href="https://github.com/jhashekhar/disaster-clf"> Disaster Classification </a> on tweet dataset.<br/><br/>

<a href="https://github.com/jhashekhar"> Github  </a> / <a href="https://linkedin.com/in/jhas"> Linkedin </a> / <a href="https://kaggle.com/xanthate"> Kaggle</a> / <a href="blog.html"> Blog</a></p>

<h3>Recent Posts</h3>

{% for post in site.posts limit:2 %}
<table>
  <tr>
    <td><img src="{{ post.image }}"></td>
    <td><p><a href="{{ post.url }}"> {{ post.title }} </a> | {{ post.date | date: "%b %d, %Y" }} <br/>
    {{ post.content | strip_html | truncatewords: 40 }}
    </p></td>
  </tr>
</table>
{% endfor %}
