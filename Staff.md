---
title: Staff
layout: default
nav_order: 5
permalink: /staff/
---

# Course Staff

## Instructor

<div class="staff-grid staff-grid--instructor">
  {% for person in site.data.staff.instructors %}
  <article class="staff-card staff-card--instructor">
    <div class="staff-avatar" aria-hidden="true">{{ person.name | slice: 0 }}</div>
    <div class="staff-details">
      <h3>{{ person.name }}</h3>
      <p class="staff-role">Instructor</p>
      <a href="mailto:{{ person.email }}">{{ person.email }}</a>
      {% if person.office %}<p class="staff-meta">{{ person.office }}</p>{% endif %}
    </div>
  </article>
  {% endfor %}
</div>

## Teaching Assistants

<div class="staff-grid">
  {% for person in site.data.staff.teaching_assistants %}
  <article class="staff-card">
    <div class="staff-avatar staff-avatar--ta" aria-hidden="true">{{ person.name | slice: 0 }}</div>
    <div class="staff-details">
      <h3>{{ person.name }}</h3>
      <p class="staff-role">Teaching Assistant</p>
      <a href="mailto:{{ person.email }}">{{ person.email }}</a>
    </div>
  </article>
  {% endfor %}
</div>
