---
permalink: /publications/
title: "Publications"
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/Publications_shutterstock.jpg
---

{% for publication in site.publications %}
  <div>
    <h2>
      <a href="/horizon-europe-2023-ire{{ publication.url }}">{{ publication.title }}</a>
    </h2>
    <p style="font-size: 14px;">Written by: {{ publication.authors }}</p>
  </div>
{% endfor %}