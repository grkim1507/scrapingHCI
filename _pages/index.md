---
layout: page
title: Home
id: home
permalink: /
---

# Welcome! 🌱

<p style="padding: 3em 1em; background: #ffac1c; border-radius: 4px;">
  This is Garyoung Kim's HCI Class Scrapbook!
  Take a look at <span style="font-weight: bold">[[Case studies]]</span> to get started on your exploration.
</p>

<strong>Recently updahttps://scrapinghci.netlify.app/case-studiested notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
