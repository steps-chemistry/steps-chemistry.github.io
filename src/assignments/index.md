---
layout: base.njk
title: Labs
---

# Guided Exploration Labs

Hands-on activities designed to deepen your understanding of mathematical concepts through exploration and discovery.

## Available Labs

{% for lab in collections.labs | sort(false, false, 'data.date') %}
{% if lab.data.title != "Labs" %}
<div class="content-card">
<h3><a href="{{ lab.url }}">{{ lab.data.title }}</a></h3>
<p>{{ lab.data.description }}</p>
<p class="lab-date"><strong>Date:</strong> {{ lab.data.date | dateFormat }}</p>
</div>
{% endif %}
{% endfor %}