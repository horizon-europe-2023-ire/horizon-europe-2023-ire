---
permalink: /news/
title: News
layout: splash
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/Publications_shutterstock.jpg
  caption: "Photo Credit: Shutterstock"
---
<div style="max-width: 75%; margin: 0 auto;">
    <ul class="post-list" style="list-style: none; padding: 0;">
      {% for post in site.posts limit:5 %}
        <li class="post-item" style="display: flex; margin-bottom: 40px; border: 1px solid #ccc; border-radius: 8px; overflow: hidden;">
          <div class="post-thumbnail" style="flex: 0 0 auto; margin-right: 20px; width: 250px; display: flex; justify-content: center; align-items: center; margin-left: 20px;">
            <img src="{{ post.image | relative_url}}" alt="{{ post.title }}" style="height: 80%; object-fit: cover;">
          </div>
          <div class="post-content" style="flex: 1 1 auto; margin-top: 0; margin-bottom: 0; padding: 50px;">
            <p class="post-title" style="font-size: 1em; margin-bottom: 10px; font-weight: bold;"><a href="{{ post.url }}">{{ post.title }}</a></p>
            <p class="excerpt" style="font-size: 0.8em; margin-top: 5px;">{{ post.excerpt }}</p>
          </div>
        </li>
      {% endfor %}
    </ul>
</div>
