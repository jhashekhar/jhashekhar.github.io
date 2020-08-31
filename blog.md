---
layout: post
title: Blog
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

{% for post in site.posts %}
<table id="menu">
  <tr>
    <!--<td width="180px" height="160px"><img src="{{ post.image }}"></td>-->
    <td><p><a href="{{ post.url }}"> {{ post.title }} </a> <!-- | {{ post.date | date: "%b %d, %Y" }} <br>
    {{ post.content | strip_html | truncatewords: 20 }}-->
    </p></td>
  </tr>
</table>
{% endfor %}
