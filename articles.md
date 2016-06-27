---
layout: default
title: Articles
permalink: /articles/
---

<div class="two-column">


<div class="col-left">
  <article class="post-content">
    <ul class="post-list">
      {% for post in site.categories.articles %}
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



</div>
