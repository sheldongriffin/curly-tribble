---
layout: default
title: "Home"
---

# Welcome to My Book

Here is the Table of Contents:

{% for chapter in site.chapters | sort: 'date' | sort: 'title' %}
- [{{ chapter.title }}]({{ site.baseurl }}{{ chapter.url }}) - {{ chapter.date | date: "%B %d, %Y" }}
{% endfor %}
