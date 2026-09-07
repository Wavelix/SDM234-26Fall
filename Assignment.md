---
title: Assignment
layout: default
nav_order: 3
permalink: /assignment/
---

# Assignment

<div class="course-module">
  <dl>
    {% for assignment in site.data.assignments.assignments %}
    <dt>{{ assignment.title }}</dt>
    <dd>
      <div class="course-resource">
        <span class="course-resource__title"><strong class="label label-red">DDL</strong>{{ assignment.ddl }}</span>
        {% if assignment.file %}
        <a class="course-resource__download" href="{{ assignment.file | relative_url }}" download>Download</a>
        {% endif %}
      </div>
    </dd>
    {% endfor %}
  </dl>
</div>
