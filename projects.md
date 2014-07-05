---
layout: page
title: Projects
permalink: /projects/
---

{% for repo in site.data.repos %}
## [{{ repo.name }}]({{ repo.html_url }})

{{ repo.description }}

Language: {{ repo.language }}
{% endfor %}
