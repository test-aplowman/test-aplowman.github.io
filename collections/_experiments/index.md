---
layout: collection_home
title: Experiments
page_width: wide
show_breadcrumbs: false
show_meta: false
---

{% include get_checklists.html %}

{% assign site_url_split = site.url | split: "https://" %}
{% assign prose_new_url = "https://prose.io/#" | append: site.github_user_or_organisation | append: "/" | append: site_url_split[1] | append: "/new/master/_includes/checklists/" %}

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
        {% assign exp_title_nospace = exp.title | replace: " ", "-" -%}
        {% assign cl_add_url = prose_new_url | append: exp_title_nospace | append: ".yml" -%}
        {% assign checklist_col = "[add](" | append: cl_add_url | append: ")" -%}
        {% for cl in checklists -%}            
            {% if cl == exp_title_nospace -%}
                {% assign checklist_col = "view \| edit" -%}
            {% endif -%}
        {% endfor -%}
        | [{{ exp.title }}]({{ exp.url }}) | {{ exp.author }} | {{ checklist_col }} | {{ an_code_link }} |
    {% endif -%}
{% endfor -%}

