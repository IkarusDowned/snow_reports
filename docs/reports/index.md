---
---
# Reports

{% assign report_pages = site.pages | where_exp: "p", "p.path contains 'reports/'" | where_exp: "p", "p.name != 'index.md'" | sort: "name" | reverse %}
{% for p in report_pages %}
{% assign area = p.path | split: "/" | slice: 1, 1 | first %}
- [{{ area | replace: "-", " " | capitalize }}: {{ p.title | default: p.name | replace: ".md", "" | replace: "_", " " }}]({{ p.url | relative_url }})
{% endfor %}
