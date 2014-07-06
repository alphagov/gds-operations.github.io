---
layout: page
title: Projects
permalink: /projects/
---

{% assign sorted_repos = site.data.repos | sort: 'name' %}

{% for repo in sorted_repos %}
## [{{ repo.name }}]({{ repo.html_url }})

{{ repo.description }}

Language: {{ repo.language }}
{% endfor %}
