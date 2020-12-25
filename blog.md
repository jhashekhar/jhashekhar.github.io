---
layout: post
title: Blog
---

<!-- <h3 align="center"><u>Posts</u></h3><br> -->
<br>
<h3 style="margin-left: 0.8em;">Blog</h3>
{% for post in site.posts %}
<table id="menu">
  <tr>
    <td><p><a href="{{ post.url }}"> {{ post.title }} </a>
    </p></td>
  </tr>
</table>
{% endfor %}
