---
layout: page
title: Table test
permalink: /awards/
description:
---
Awards given at the Music Encoding Conference are listed below

<table>
{% for row in site.data.awards %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>