---
layout: collection_home
title: Experiments
page_width: wide
show_breadcrumbs: false
show_meta: false
---

| Experiment | Champion | Metadata template | Analysis code |
| ---------- | -------- | ----------------- | ------------- |
{% for exp in site.experiments -%}
    {% assign filename = exp.url | split: "/" -%}
    {% if filename[-1] != "index" -%}
        {% assign exp_name = filename[-1] | split: ".html" -%}
        | [{{ exp.title }}]({{ exp.url }}) | {{ exp.author }} | [Download](/checklists/{{ exp_name[0] | append: '.yml' }}) | [Link]({{ exp.analysis_code }}) |
    {% endif %}
{% endfor %}

<a href="http://prose.io/#test-aplowman/test-aplowman.github.io/tree/master/_posts" class="add-exp-button">+ add experiment</a>
