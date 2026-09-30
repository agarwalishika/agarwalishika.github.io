---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: false
---

{% include base_path %}

<p class="page__lead">
  Smaller studies, course projects, and my master's thesis — work that didn't become a full paper
  but that I still think is worth reading.
</p>

{% assign projects = site.projects | sort: "date" | reverse %}
{% assign years = projects | group_by_exp: "p", "p.date | date: '%Y'" %}

{% for year in years %}
  <div class="yeargroup">
    <h2 class="yeargroup__label">{{ year.name }}</h2>
    <div class="pubs">
      {% for post in year.items %}
        {% include pub-card.html %}
      {% endfor %}
    </div>
  </div>
{% endfor %}
