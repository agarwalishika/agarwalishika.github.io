---
layout: archive
title: "Sitemap"
permalink: /sitemap/
author_profile: false
---

{% include base_path %}

<p class="page__lead">
  Everything on this site. There's an <a href="{{ base_path }}/sitemap.xml">XML version</a> for robots.
</p>

<div class="yeargroup">
  <h2 class="yeargroup__label">Pages</h2>
  <ul>
    {% for p in site.pages %}
      {% if p.title and p.permalink %}
        <li><a href="{{ base_path }}{{ p.url }}">{{ p.title }}</a></li>
      {% endif %}
    {% endfor %}
  </ul>
</div>

{% for collection in site.collections %}
  {% if collection.output != false and collection.docs.size > 0 %}
    <div class="yeargroup">
      <h2 class="yeargroup__label">{{ collection.label | capitalize }}</h2>
      <ul>
        {% for doc in collection.docs %}
          <li><a href="{{ base_path }}{{ doc.url }}">{{ doc.title }}</a></li>
        {% endfor %}
      </ul>
    </div>
  {% endif %}
{% endfor %}
