---
layout: team
permalink: /team/index.html
title: People
tagline: A List of People
tags: [blog, graphic design]
---

<h1 itemprop="name">{{ page.title }}</h1>
   
<h3>Current Members</h3>

<article itemscope itemtype="http://schema.org/BlogPosting" itemprop="blogPost" class="article-author">
{% include _author-bio.html %}
</article>

  {% for member in site.members %}
<article itemscope itemtype="http://schema.org/BlogPosting" itemprop="blogPost">
      {% if member.avatar %}<h5><img src="{{ site.url }}/images/{{ member.avatar }}" class="team-photo" alt="{{ member.name }} bio photo"></h5>{% endif %}
      {% if member.url %}
        <h2><a href="{{ member.url }}" rel="bookmark" target="_blank">{{ member.name }}</a>
        {% if member.email %}
          <a href="mailto:{{ member.email }}" target="_blank"><i class="icon-mail"></i></a>
        {% endif %}
        </h2>
      {% else %}
        <p itemprop="text">{{ member.name }}
        {% if member.email %}
          <a href="mailto:{{ member.email }}" target="_blank"><i class="icon-mail"></i></a>
        {% endif %}
        </p>
      {% endif %}
      <p itemprop="text">{{ member.bio }}</p>
</article>
  {% endfor %}

<h3>Alumni</h3>


  {% for member in site.alumna %} 
<article itemscope itemtype="http://schema.org/BlogPosting" itemprop="blogPost">
      {% if member.avatar %}<h5><img src="{{ site.url }}/images/{{ member.avatar }}" class="alumni-photo" alt="{{ member.name }} bio photo"></h5>{% endif %}
      {% if member.url %}
        <h2><a href="{{ member.url }}" rel="bookmark" target="_blank">{{ member.name }}</a>
        {% if member.email %}
          <a href="mailto:{{ member.email }}" target="_blank"><i class="icon-mail"></i></a>
        {% endif %}
        </h2>
      {% else %}
        <p itemprop="text">{{ member.name }}
        {% if member.email %}
          <a href="mailto:{{ member.email }}" target="_blank"><i class="icon-mail"></i></a>
        {% endif %}
        </p>
      {% endif %}
      <p itemprop="text">{{ member.bio }}</p>
</article>
  {% endfor %}