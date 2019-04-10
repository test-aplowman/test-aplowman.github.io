---
layout: collection_home
title: Experiments
page_width: wide
show_breadcrumbs: false
show_meta: false
---

{% include get_checklists.html %}
{% include prose_checklist_urls.html %}

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
        {% assign cl_add_url = prose_cl_new_url | append: exp_title_nospace | append: ".yml" -%}
        {% assign cl_edit_url = prose_cl_edit_url | append: exp_title_nospace | append: ".yml" -%}        
        {% assign checklist_col = "[add](" | append: cl_add_url | append: ")" -%}
        {% for cl in checklists -%}            
            {% if cl == exp_title_nospace -%}
                {% assign view_link = exp.url | append: "#checklist" -%}
                {% assign checklist_col = "[view](" | append: view_link | append: ")" -%}
                {% assign checklist_col = checklist_col | append: " \| [edit](" | append: cl_edit_url | append: ")" -%}
                {% assign checklist_col = checklist_col | append: " \| [delete](" | append: prose_cl_dir_url | append: ")" -%}
            {% endif -%}
        {% endfor -%}
        | [{{ exp.title }}]({{ exp.url }}) | {{ exp.author }} | {{ checklist_col }} | {{ an_code_link }} |
    {% endif -%}
{% endfor -%}

