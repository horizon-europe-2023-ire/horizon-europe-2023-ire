---
permalink: /publications/
title: "Publications"
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/main_image.png
  caption: "Photo credit:"
---

{% for publication in site.publications %}
  <div>
    <h2>
      <a href="{{ publication.url }}">{{ publication.title }}</a>
    </h2>
    <p style="font-size: 14px;">Written by: {{ publication.authors }}</p>
  </div>
{% endfor %}