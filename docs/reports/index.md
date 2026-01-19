---
---
# Reports

{% assign location_indexes = site.pages | where_exp: "p", "p.path contains 'reports/'" | where_exp: "p", "p.path contains '/index.md'" | where_exp: "p", "p.path != 'reports/index.md'" | sort: "path" %}
{% for p in location_indexes %}
{% assign location = p.path | split: "/" | slice: 1, 1 | first %}
- [{{ location | replace: "-", " " | capitalize }}]({{ p.url | relative_url }})
{% endfor %}
