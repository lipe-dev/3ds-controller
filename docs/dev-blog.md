---
layout: default
title: 📰 Dev-Blog
---
# 📰 Latest Updates

Here is what new about this project:

{% for post in site.posts %}
## [{{ post.title }}]({{site.baseurl}}{{ post.url }})

<p style="color: cadetblue; font-size: 10pt">📅 
 {{ post.date | date_to_string }} - {{ post.author }}
</p>

{{ post.excerpt }}
{% endfor %}
