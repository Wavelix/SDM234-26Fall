---
title: Schedule
layout: default
nav_order: 4
permalink: /schedule/
---

# Weekly Schedule

<div class="schedule" aria-label="Weekly class schedule">
  <div class="schedule-board">
    <ol class="schedule-timeline" aria-hidden="true">
      {% for time in site.data.schedule.timeline %}
      <li><span>{{ time }}</span></li>
      {% endfor %}
    </ol>
    <div class="schedule-days">
      {% for day in site.data.schedule.days %}
      <section class="schedule-day">
        <h2>{{ day.name }}</h2>
        <div class="schedule-events">
          {% for event in day.events %}
          {% assign start_parts = event.start | split: ':' %}
          {% assign end_parts = event.end | split: ':' %}
          {% assign start_minutes = start_parts[0] | times: 60 | plus: start_parts[1] %}
          {% assign end_minutes = end_parts[0] | times: 60 | plus: end_parts[1] %}
          {% assign event_top = start_minutes | minus: 960 | times: 8 | divided_by: 5 %}
          {% assign event_height = end_minutes | minus: start_minutes | times: 8 | divided_by: 5 %}
          <article class="schedule-event" style="top: {{ event_top }}px; height: {{ event_height }}px;">
            <strong>{{ event.name }}</strong>
            <span>{{ event.start }}–{{ event.end }}</span>
            <span>{{ event.location }}</span>
          </article>
          {% endfor %}
        </div>
      </section>
      {% endfor %}
    </div>
  </div>
</div>
