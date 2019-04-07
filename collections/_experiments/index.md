---
layout: collection_home
title: Experiments
page_width: wide
show_breadcrumbs: false
show_meta: false
---

{% assign exp_sorted = site.experiments | sort: "title" %}

| Experiment | Champion | Metadata template | Analysis code |
| ---------- | -------- | ----------------- | ------------- |
{% for exp in exp_sorted -%}
    {% assign filename = exp.url | split: "/" -%}
    {% if filename[-1] != "index" -%}
        {% assign exp_name = filename[-1] | split: ".html" -%}
        {% assign an_code_link = "-" -%}
        {% if exp.analysis_code -%}
            {% assign an_code_link = '[Link](' | append: exp.analysis_code | append: ')' -%}
        {% endif -%}
        | [{{ exp.title }}]({{ exp.url }}) | {{ exp.author }} | [Download](/checklists/{{ exp_name[0] | append: '.yml' }}) | {{ an_code_link }} |
    {% endif -%}
{% endfor -%}

{% assign site_url_split = site.url | split: "https://" %}
{% assign prose_new_check_url = "https://prose.io/#" | append: site.github_user_or_organisation | append: "/" | append: site_url_split[1] | append: "/new/master/checklists" %}

<!-- http://prose.io/#test-aplowman/test-aplowman.github.io/new/master/checklists -->

<a href="{{ prose_new_check_url }}" class="add-exp-button">+ add checklist</a>