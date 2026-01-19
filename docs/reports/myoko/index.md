---
---
# Myoko Reports

{% assign reports = site.pages | where_exp: "p", "p.path contains 'reports/myoko/'" | where_exp: "p", "p.name != 'index.md'" | sort: "name" | reverse %}
{% for p in reports %}
- [{{ p.title | default: p.name | replace: ".md", "" | replace: "_", " " }}]({{ p.url | relative_url }})
{% endfor %}
