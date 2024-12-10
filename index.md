---
layout: my-fancy-layout
title: "Home"
---

# Welcome to My Book

Here is the Table of Contents:

{% assign sorted_chapters = site.chapters | sort: 'date' | reverse %}
{% for chapter in sorted_chapters %}
- [{{ chapter.title }}]({{ site.baseurl }}{{ chapter.url }}) - {{ chapter.date | date: "%B %d, %Y" }}
{% endfor %}
