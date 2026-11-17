---
layout: page
title: Calendar
description: Listing of course modules and topics.
nav_order: 1
parent: Fall 2025
---

# Calendar

*This page is an archive of the Fall 2025 offering of the course. See the [current course website](/).*

**Subject to change.**

{% for module in site.fall2025_modules %}
{{ module }}
{% endfor %}
