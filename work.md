---
layout: page
title: Work
description: Experienced in building products and services in various domains like e-commerce, education, fintech, legal, and social networks.
permalink: /work/
---

<article class="mdc-layout-grid" style="--mdc-layout-grid-margin: 0 0 16px 0;">
{% for client in site.clients %}
  <div class="mdc-layout-grid__cell mdc-layout-grid__cell--span-4 mdc-layout-grid__cell--span-4-phone">
    <img alt="{{ post.client }}" src="{{ site.url }}/assets/img/{{ client[1].logo }}" style="border: 1px solid #e4e4e4;" />
  </div>
  <div class="mdc-layout-grid__cell mdc-layout-grid__cell--span-8 mdc-layout-grid__cell--span-4-phone">
    <h3 style="margin-top: 0;">{{ client[1].name | escape }}</h3>
    <p>{{ client[1].about }}</p>
    <ul class="list-unstyled">
      {% assign posts = (site.posts | where: "client" , client[1].name) %}
      {% for post in posts %}
        <li>
          {{ post.date | date: "%Y" }} <a href="{{ post.url }}">{{ post.title }}</a>
        </li>
      {% endfor %}
    </ul>
  </div>
{% endfor %}
</article>