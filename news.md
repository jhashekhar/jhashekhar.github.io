---
layout: news
title: News
---
<style>
#menu img {
    display: block;
    width: 100%;
    height: 100%;
  }
</style>

<!-- <h3 align="center"><u>Posts</u></h3><br> -->
<br><br>
<h3 style="margin-left: 0.8em;">News</h3>
{% for post in site.posts %}
<table id="menu">
  <tr>
    <td><p><a href="{{ post.url }}"> {{ post.title }} </a>
    </p></td>
  </tr>
</table>
{% endfor %}
