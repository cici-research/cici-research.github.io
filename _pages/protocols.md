---
title: "Protocols"
permalink: /protocols/
---

我会在这里更新一些湿实验的protocols，除了通用的分子生物学实验，更注重心肌细胞与心脏研究的相关实验。

{% assign protocols = site.protocols | sort: "date" | reverse %}
{% for protocol in protocols %}

## [{{ protocol.title }}]({{ protocol.url | relative_url }})

{% if protocol.date %}
*{{ protocol.date | date: "%Y-%m-%d" }}*
{% endif %}

{{ protocol.excerpt }}

---

{% endfor %}