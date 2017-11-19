---
layout: page
title: Market Notes
---

{% for post in site.posts %}
<div class="pa4 br3 mb4 bg-chalk">
  <h2 class="mt0 tc"><a class="link dim" href="{{ post.url }}">{{ post.title }}</a></h2>
  <p class="tc f5">{{ post.author }} | {{ post.date | date: "%-d %B, %Y" }}</p>
  {% if post.featured-image %}
  <a href="{{ post.url }}"><img src="/images/{{ post.featured-image }}"></a>
  {% endif %}
  <p>{{ post.excerpt }}</p>
  <div class="tc">
    <a class="dib no-underline bg-wintergreen white br3 tc f3 f5 pv2 ph3 b grow shadow-gravel" href="{{ post.url }}">Read more</a>
  </div>
</div>
{% endfor %}
