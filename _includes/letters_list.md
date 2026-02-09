<ul>
{% assign pages = site.pages | where_exp: "p", "p.path contains 'letters/'" %}
{% for p in pages %}
  {% if p.url != '/letters/' %}
  <li><a href="{{ p.url | relative_url }}">{{ p.title }}</a> — {{ p.date | date: "%Y-%m-%d" }}</li>
  {% endif %}
{% endfor %}
</ul>