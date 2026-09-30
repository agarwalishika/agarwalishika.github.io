---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: false
---

{% include base_path %}

<p class="page__lead">
  Also on <a href="{{ site.author.googlescholar }}">Google Scholar</a>. * denotes equal contribution.
</p>

{% assign pubs = site.publications | sort: "date" | reverse %}
{% assign years = pubs | group_by_exp: "p", "p.date | date: '%Y'" %}

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
