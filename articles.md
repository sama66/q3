---
layout: default
title: Articles
permalink: /articles/
---

<div class="two-column">


<div class="col-left">
  <article class="post-content">
    {% if page.img %}<img src="{{ site.baseurl }}/asset/img/medium/{{ page.img.medium }}">{% endif %}
    <ul class="post-list">
      {% for post in site.posts %}
        <li>
          <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
          <h2><a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h2>
          <p>{{ post.excerpt }}</p>
        </li>
      {% endfor %}
    </ul>
    <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>
  </article>
</div>

<div class="col-right">
  <div class="clearfix">
    {% for category in site.categories %}
    <li><span class="sidebar">{{ category | first }}</span>
      <ul>
        {% for posts in category %}
        {% for post in posts %}
        <li><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></li>
        {% endfor %}
        {% endfor %}
      </ul>
    </li>
  {% endfor %}
  </div>
</div>

</div>
