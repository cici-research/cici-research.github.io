---
title: "Thoughts"
permalink: /thoughts/
---

{% for post in site.posts %}

## [{{ post.title }}]({{ post.url }})

{{ post.excerpt }}

---

{% endfor %}