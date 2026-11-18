---
title: "News"
layout: textlay
excerpt: "Ní Leathlobhair Lab at Trinity College Dublin."
sitemap: false
permalink: /allnews.html
---

# News

<div class="news-archive" markdown="0">
{% for article in site.data.news %}
<div class="news-archive-entry">
<strong>{{ article.date }}</strong>
{{ article.headline | markdownify }}
</div>
{% endfor %}
</div>
