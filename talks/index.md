---
layout: page
title: Talks
permalink: /talks/
---

Titles and abstracts marked as to be determined will be updated once finalized.

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
            To be determined
          {% endif %}
        </li>
      {% endif %}
    {% endfor %}
  {% endfor %}
</ul>
