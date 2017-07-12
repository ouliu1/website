---
layout: team
permalink: /team/index.html
title: People
tagline: A List of People
tags: [blog, graphic design]
---

<h1 itemprop="name">{{ page.title }}</h1>
   
<h3>Current Members</h3>


  {% for member in site.members %} 
<article itemscope itemtype="http://schema.org/BlogPosting" itemprop="blogPost">
      <h5><img src="{{ site.url }}/images/{{ site.owner.avatar }}" class="bio-photo" alt="{{ site.owner.name }} bio photo"></h5>
      <h2 itemprop="headline"><a href="{{ site.url }}{{ post.url }}" rel="bookmark" title="{{ post.title }}">{{ member.name }}</a></h2>
      <p itemprop="text">{{ member.bio }}</p>
</article>
  {% endfor %}

<h3>Alumna</h3>


  {% for member in site.alumna %} 
<article itemscope itemtype="http://schema.org/BlogPosting" itemprop="blogPost">
      <h2 itemprop="headline"><a href="{{ site.url }}{{ post.url }}" rel="bookmark" title="{{ post.title }}">{{ member.name }}</a></h2>
      <p itemprop="text">{{ member.bio }}</p>
</article>
  {% endfor %}