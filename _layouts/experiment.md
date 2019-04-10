---
layout: post
---

{{ content }}

{% include get_checklists.html %}

{% assign checklist_name = page.title | replace: " ", "-" -%}

{% for cl in checklists -%}
{% if cl == checklist_name -%}
  {{ "## Checklist" | markdownify }}
  {% capture my_include %}{% include checklist.md checklist=checklist_name %}{% endcapture %}
  {{ my_include | markdownify }}
{% endif -%}
{% endfor %}
