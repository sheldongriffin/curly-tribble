---
layout: default
title: "Table of Contents"
---
# Table of Contents

{% for chapter in site.chapters %}
- [{{ chapter.title }}]({{ chapter.url }}) - {{ chapter.date | date: "%B %d, %Y" }}
{% endfor %}
