---
layout: post
title: Blog
---

<h3>Posts</h3>

{% for post in site.posts %}
<table>
  <tr>
    <td><img src="{{ post.image }}"></td>
    <td><p><a href="{{ post.url }}"> {{ post.title }} </a> | {{ post.date | date: "%b %d, %Y" }} <br/>
    {{ post.content | strip_html | truncatewords: 40 }}
    </p></td>
  </tr>
</table>
{% endfor %}