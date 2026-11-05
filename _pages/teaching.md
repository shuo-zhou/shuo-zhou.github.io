---
layout: page
permalink: /teaching/
title: Teaching
# description: Teaching Materials (Pending)
nav: true
nav_order: 4
calendar: true
---

<!-- title: teaching
description: Course materials, schedules, and resources for classes taught.
nav: true
nav_order: 6
calendar: true
---

<!-- This page displays a collection of courses with detailed schedules, materials, and resources. You can organize your courses by years, terms, or topics. -->

{% include courses.liquid %}

{% if site.data.teaching_repo.github_repos %}

<div class="teaching d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.teaching_repo.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}

{% include calendar.liquid calendar_id='shuo.zhou@sheffield.ac.uk' timezone='Europe/London' %}
