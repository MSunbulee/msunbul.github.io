---
layout: page
title: "Projects"
permalink: /portfolio/projects/
---

Below are selected projects. Each page includes problem framing, approach, my role, and results with metrics.

<ul>
  {%- assign items = site.projects | sort: "order" -%}
  {%- for p in items -%}
    <li style="margin:0.5rem 0;">
      <a href="{{ p.url | relative_url }}"><strong>{{ p.title }}</strong></a>
      {%- if p.year %} <span style="color:#666;"> · {{ p.year }}</span>{% endif -%}
      {%- if p.affiliation %} <span style="color:#666;"> · {{ p.affiliation }}</span>{% endif -%}
      <br>
      {%- if p.summary %}<span style="color:#555;">{{ p.summary }}</span>{% endif -%}
    </li>
  {%- endfor -%}
</ul>
