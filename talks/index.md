---
layout: page
title: talks
permalink: /talks/
---

# Talks

Titles and abstracts marked as to be confirmed will be updated once finalized.

## Abstracts

<ul>
  {% for day in site.data.schedule.days %}
    {% for slot in day.slots %}
      {% if slot.talk %}
        {% assign talk_permalink = '/talks/' | append: slot.talk | append: '/' %}
        {% assign talk_pages = site.pages | where: 'permalink', talk_permalink %}
        {% assign talk = talk_pages | first %}
        <li>
          {% if talk %}
            <a href="{{ talk.permalink | relative_url }}">{{ talk.speaker }}, &quot;{{ talk.title }}&quot;</a>
          {% else %}
            To be confirmed
          {% endif %}
        </li>
      {% endif %}
    {% endfor %}
  {% endfor %}
</ul>
