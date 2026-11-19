---
title: Welcome to our travel blog!
layout: page
---
**Travelling the World, again!**

<img src="{{ "/assets/images/bus_spiderman_450.png" | relative_url }}"
     alt="local bus in Mahébourg, Mauritius."
     width="600">

{% assign cutoff = 20260501 %}

## Mauritius 2026
{% for post in site.posts %}
{% assign d = post.date | date: "%Y%m%d" | plus: 0 %}
{% if d >= cutoff %}
- {{ post.date | date: "%b %-d" }} · [{{ post.title }}]({{ post.url | relative_url }})
{% endif %}
{% endfor %}

<details markdown="1">
<summary><strong>Bahamas Island Hopping 2026</strong></summary>

{% for post in site.posts %}
{% assign d = post.date | date: "%Y%m%d" | plus: 0 %}
{% if d < cutoff %}
- {{ post.date | date: "%b %-d" }} · [{{ post.title }}]({{ post.url | relative_url }})
{% endif %}
{% endfor %}

</details>
