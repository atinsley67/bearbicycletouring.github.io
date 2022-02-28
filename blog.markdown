---
layout: page
title: Blog
image: /assets/images/blogBanner.jpg
imageTxt: Our blog
---
<h1>Latest Posts</h1>

<ul>
  {% for post in site.posts %}
    <li>
	  <!--<img src="/assets/images/blog/{{post.blogImage}}_small.jpg" align="left">-->
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>