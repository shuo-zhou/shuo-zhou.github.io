---
layout: page
permalink: /teaching/
title: Teaching
# description: Teaching Materials (Pending)
nav: true
nav_order: 4
---

<!-- For now, this page is assumed to be a static description of your courses. You can convert it to a collection similar to `_projects/` so that you can have a dedicated page for each course.

Organize your courses by years, topics, or universities, however you like! -->

<!-- <article> -->
<div class="cv">
  {% for entry in site.data.teaching %}
    <div class="card mt-3 p-3">
      <h3 class="card-title font-weight-medium">{{ entry.title }}</h3>
      <div>
        {% if entry.type == "list" %}
        {% include cv/list.liquid %}
        {% elsif entry.type == "map" %}
        {% include cv/map.liquid %}
        {% elsif entry.type == "nested_list" %}
        {% include cv/nested_list.liquid %}
        {% elsif entry.type == "time_table" %}
        {% include cv/time_table.liquid %}
        {% else %}
        {{ entry.contents }}
        {% endif %}
      </div>
    </div>
  {% endfor %}
</div>
<!-- </article> -->

{% if site.data.teaching_repo.github_repos %}

<div class="teaching d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.teaching_repo.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
