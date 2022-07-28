---
layout: default
title: Dev-Blog
---
# Latest Updates

Here is what new about this project:

{% for post in site.posts %}
## [{{ post.title }}]({{ post.url }})
> {{ post.date | date_to_string }} - {{ post.author }}

{{ post.excerpt }}
{% endfor %}
