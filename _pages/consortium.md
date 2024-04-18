---
permalink: /consortium/
title: "Consortium"
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/Events_shutterstock.jpg
---

{% for collaborator in site.collaborators %}
  <h2>{{ collaborator.institution }}</h2>
  <div>
    <div style="display: flex; align-items: center; justify-content: space-between; height: 100%; padding: 20px; font-size: 16px; line-height: 1;">
      <img src="{{ collaborator.img_path }}" alt="logo" class="flag" style="max-height: 150px; vertical-align: middle;">
      <div style="flex: 1; margin-left: 40px; margin-right: 40px;">
        <p> Role: {{ collaborator.role }} </p>
        <p>Country: {{ collaborator.country }}</p>
        <a href="{{ collaborator.link }}" class="btn btn--inverse">more</a>
      </div>
    </div>
    {% if collaborator.description %}
      <p>{{ collaborator.description | markdownify | strip }}</p>
    {% endif %}
  </div>
{% endfor %}
