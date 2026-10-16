---
title: "Bioinformatics"
permalink: /bioinformatics/
author_profile: true
---

这里记录我使用 R 语言进行的生物信息学分析，包括代码、数据说明和分析结果。

{% assign analyses = site.bioinformatics | sort: "date" | reverse %}
{% for analysis in analyses %}

## [{{ analysis.title }}]({{ analysis.url | relative_url }})

{% if analysis.date %}
*{{ analysis.date | date: "%Y-%m-%d" }}*
{% endif %}

{% if analysis.tags %}
标签：{% for tag in analysis.tags %}`{{ tag }}` {% endfor %}
{% endif %}

{{ analysis.excerpt }}

---

{% endfor %}
