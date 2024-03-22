---
permalink: /events/
title: "Events"
layout: splash
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/main_image.png
  caption: "Photo credit:"
excerpt: "Bacon ipsum dolor sit amet salami ham hock ham, hamburger corned beef short ribs kielbasa biltong t-bone drumstick tri-tip tail sirloin pork chop."
intro:
  - excerpt: 'Here are the events.'
---

{% include feature_row id="intro" type="center" %}

<ul>
  {% for post in site.posts limit:1 %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

