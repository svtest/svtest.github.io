---
layout: page
title : Literatur
header : Literatur
category: Aktuelles
---

<div class="page-header">
  <h3>{{ page.title }} {% if page.tagline %} <small>{{ page.tagline }}</small>{% endif %}</h3>
</div>

<div>
{% for tag in site.tags %} 
  {% if page.title == tag[0] %}
  <ul class="unstyled">
{% comment %}
    {% assign pages_list = tag[1] %}  
    {% include JB/pages_list %}
{% endcomment %}  
    <br />
  </ul>
  {{tag[1]}}<br /><br />
  {% endif %}
{% endfor %}
</div>

<div class="pagination">
    <ul>
      <li><a href="/aktuelles.html">Aktuelles</a></li>
    </ul>
  </div>
   
{% include JB/comments %}

