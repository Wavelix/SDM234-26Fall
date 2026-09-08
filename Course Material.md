---
title: Course Material
layout: default
nav_order: 2
permalink: /course-material/
---

# Course Material

<div class="course-module">
  <dl>
    {% assign textbook = site.data.course_materials.textbook %}
    <dt>Reference</dt>
    <dd>
      <div class="course-resource">
        <span class="course-resource__title course-resource__title--material"><strong class="label">Textbook</strong>{{ textbook.title }}</span>
        {% if textbook.file %}
        <a class="course-resource__download" href="{{ textbook.file | relative_url }}" download>Download</a>
        {% endif %}
      </div>
    </dd>
    {% for lecture in site.data.course_materials.lectures %}
    <dt>{{ lecture.label }}</dt>
    <dd>
      <div class="course-resource">
        <span class="course-resource__title course-resource__title--material"><strong class="label label-purple">Slides</strong>{{ lecture.title }}</span>
        {% if lecture.file %}
        <a class="course-resource__download" href="{{ lecture.file | relative_url }}" download>Download</a>
        {% endif %}
      </div>
    </dd>
    {% endfor %}
  </dl>
</div>
