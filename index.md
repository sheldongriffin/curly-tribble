---
layout: default
title: "Home"
---

# Welcome to My Book

Here is the Table of Contents:

{% for chapter in site.chapters %}
- [{{ chapter.title }}]({{ chapter.url }}) - {{ chapter.date | date: "%B %d, %Y" }}
{% endfor %}
