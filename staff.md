---
layout: page
title: Oktatók
description: Oktatók listája.
---

# Oktatók

## Kurzustartó

{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

{% assign teaching_assistants = site.staffers | where: 'role', 'Teaching Assistant' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}

## Tanársegédek

{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}
