---
layout: page
title: Projects
permalink: /projects/
---

{% assign sorted_repos = site.data.repos | sort: 'name' %}

{% for repo in sorted_repos %}
## {{ repo.name }}

{{ repo.description }}

Language: {{ repo.language }}

Git clone URL: `{{ repo.clone_url }}`

{% if repo.homepage != nil and repo.homepage != "" %}* [Visit homepage]({{ repo.homepage }}){% endif %}
* [Git repository]({{ repo.html_url }})
{% endfor %}
