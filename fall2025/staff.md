---
layout: page
title: Staff
description: A listing of all the course staff members.
nav_order: 2
parent: Fall 2025
---

# Staff

*This page is an archive of the Fall 2025 offering of the course. See the [current course website](/).*

## Instructor

{% assign instructors = site.fall2025_staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

{% assign teaching_assistants = site.fall2025_staffers | where: 'role', 'Teaching Assistant' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}

## Teaching Assistants

{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}
