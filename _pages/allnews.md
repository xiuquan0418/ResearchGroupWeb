---
title: "News | Wang Research Group | Department of Mathematics and Computer Science at Tougaloo College"
layout: textlay
excerpt: "News | Wang Research Group | Department of Mathematics and Computer Science at Tougaloo College"
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}

<p>{{ article.date }} <br>
<em>{{ article.headline }}</em></p>
{% endfor %}
