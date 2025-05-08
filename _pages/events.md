---
permalink: /events/
title: "Events"
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/Events.jpg
  caption: "Photo Credit: DIKU"
---
<div>
  <h2>2025</h2>
</div>
{% assign entries = site.events | where:"year",2025 %}
{% assign sorted_entries = entries | sort: 'date' | reverse %}
{% for event in entries %}
  {% assign year = event.date | date: "%Y" %}
  <h3>
    <a href="{{ event.url }}">{{ event.title }}</a>
  </h3>
  <div>
      <p style="font-size: 16px;">
        <img src="../assets/images/time.png" alt="Time Icon" style="width: 16px; height: 16px; vertical-align: middle;">
        {{ event.date | date: "%A %B %d" }} at {{ event.date | date: "%-R" }} CET (UTC+1)  
        <span style="margin-right: 5px;"></span>
        <img src="../assets/images/location.png" alt="Location Icon" style="width: 16px; height: 16px; vertical-align: middle;">
        {{ event.location }}
      </p>
  </div>
{%- endfor -%}

<div>
  <h2>2024</h2>
</div>
{% assign entries = site.events | where:"year",2024 %}
{% assign sorted_entries = entries | sort: 'date' | reverse %}
{% for event in entries %}
  {% assign year = event.date | date: "%Y" %}
  <h3>
    <a href="{{ event.url }}">{{ event.title }}</a>
  </h3>
  <div>
      <p style="font-size: 16px;">
        <img src="../assets/images/time.png" alt="Time Icon" style="width: 16px; height: 16px; vertical-align: middle;">
        {{ event.date | date: "%A %B %d" }} at {{ event.date | date: "%-R" }} CET (UTC+1)  
        <span style="margin-right: 5px;"></span>
        <img src="../assets/images/location.png" alt="Location Icon" style="width: 16px; height: 16px; vertical-align: middle;">
        {{ event.location }}
      </p>
  </div>
{%- endfor -%}
