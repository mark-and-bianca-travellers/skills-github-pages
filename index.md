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

<style>
.cards{display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:1rem;margin:1rem 0}
.card{border:1px solid #ddd;border-radius:8px;overflow:hidden;text-decoration:none;color:inherit;display:block}
.card img{width:100%;height:140px;object-fit:cover;display:block}
.card .txt{padding:.6rem .8rem}
.card small{color:#777;display:block}
.card strong{display:block;margin:.2rem 0}
</style>
<div class="cards">
{% for post in site.posts %}
{% assign d = post.date | date: "%Y%m%d" | plus: 0 %}
{% if d >= cutoff %}
<a class="card" href="{{ post.url | relative_url }}">
{% if post.image %}<img src="{{ post.image | relative_url }}" alt="">{% endif %}
<div class="txt"><small>{{ post.date | date: "%b %-d" }}</small><strong>{{ post.title }}</strong>{{ post.excerpt | strip_html | truncate: 90 }}</div>
</a>
{% endif %}
{% endfor %}
</div>

<details markdown="1">
<summary><strong>Bahamas Island Hopping 2026</strong></summary>

{% for post in site.posts %}
{% assign d = post.date | date: "%Y%m%d" | plus: 0 %}
{% if d < cutoff %}
- {{ post.date | date: "%b %-d" }} · [{{ post.title }}]({{ post.url | relative_url }})
{% endif %}
{% endfor %}

</details>
