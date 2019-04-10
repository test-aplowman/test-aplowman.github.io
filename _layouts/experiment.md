---
layout: post
---
<br/>
<table class="vertical-header smaller">
  <tr>
      <th>Champion</th>
      <td>{{ page.author }}</td>
  </tr>
  <tr>
      <th>Analysis code</th>
      <td><a href="{{ page.analysis_code }}">Link</a></td>
  </tr>
</table>
<br/>

{{ content }}

{% include get_checklists.html %}
{% include prose_checklist_urls.html %}

{% assign checklist_name = page.title | replace: " ", "-" -%}

{% for cl in checklists -%}
{% if cl == checklist_name -%}
  {{ "## Checklist" | markdownify }}  
  {% assign exp_title_nospace = page.title | replace: " ", "-" -%}  
  {% assign cl_edit_url = prose_cl_edit_url | append: exp_title_nospace | append: ".yml" -%}
  <a href="{{cl_edit_url}}">Edit</a> | <a href="{{ prose_cl_dir_url }}">Delete</a>
  {% capture my_include %}{% include checklist.md checklist=checklist_name %}{% endcapture %}
  {{ my_include | markdownify }}
{% endif -%}
{% endfor %}
