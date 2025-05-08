---
permalink: /events/
title: "Events"
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/Events.jpg
  caption: "Photo Credit: DIKU"
---
{% assign events_by_year = site.events | sort: "date" | reverse %}
{% assign years = "" | split: "" %}

{% for event in events_by_year %}
  {% assign year = event.date | date: "%Y" %}
  {% unless years contains year %}
    {% assign years = years | push: year %}
  {% endunless %}
{% endfor %}

{% for year in years %}
  <div>
    <h2>{{ year }}</h2>
  </div>
  {% assign yearly_events = site.events | where_exp: "event", "event.date | date: '%Y' == year" | sort: "date" | reverse %}
  {% for event in yearly_events %}
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
  {% endfor %}
{% endfor %}
