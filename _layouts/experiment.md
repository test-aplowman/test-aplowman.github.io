---
layout: post
---

{{ content }}

{% if page.checklist -%}
  {{ "## Checklist" | markdownify }}
  {% capture my_include %}{% include checklist.md checklist=page.checklist %}{% endcapture %}
  {{ my_include | markdownify }}
{% endif -%}

the title w/o spaces: {{ page.title | replace: " ", "-" }}


