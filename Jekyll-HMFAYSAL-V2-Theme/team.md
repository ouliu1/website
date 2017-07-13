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
      <h5><img src="{{ site.url }}/images/{{ member.avatar }}" class="team-photo" alt="{{ site.owner.name }} bio photo"></h5>
      <p>
      {% if member.url %}<h2><a href="{{ member.url }}" rel="bookmark" target="_blank">{% endif %}{{ member.name }}{% if member.url %}</a>{% endif %}
      {% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="icon-mail"></i></a>{% endif %}{% if member.url %}</h2>{% endif %}
      </p>


      <p itemprop="text">{{ member.bio }}</p>
</article>
  {% endfor %}

<h3>Alumna</h3>


  {% for member in site.alumna %} 
<article itemscope itemtype="http://schema.org/BlogPosting" itemprop="blogPost">
      <p>
      {% if member.url %}<h2><a href="{{ member.url }}" rel="bookmark" target="_blank">{% endif %}{{ member.name }}{% if member.url %}</a>{% endif %}
      {% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="icon-mail"></i></a>{% endif %}{% if member.url %}</h2>{% endif %}
      </p>
      <p itemprop="text">{{ member.bio }}</p>
</article>
  {% endfor %}