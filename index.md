---
layout: default
title: tantalor.github.com
---

<style type="text/css" media="screen">
  a {
    font-weight: bold;
  }
</style>

{% if site.username %}
# {{site.username}}.github.com

My github profile: [github.com/{{site.username}}](http://github.com/{{site.username}})
{% else %}
 * missing `username` to `_config.yaml`
{% endif %}

{% if site.personal %}
My personal site: [{{site.personal|replace:"html"}}]({{site.personal}})
{% endif %}

{% if site.projects %}
## My projects

{% for project in site.projects %}
 * **[{{project.name}}](http://github.com/{{site.username}}/{{project.name}})**: {{project.desc}}
{% endfor %}
{% else %}
 * missing `projects` in `_config.yaml`
{% endif %}
