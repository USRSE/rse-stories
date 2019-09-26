---
layout: wide
title: People
permalink: /people/
form: true
---

<!-- Page Content -->
<div class="container">
  <div class="row">
  {% for person in site.people %}{% assign loopindex = forloop.index | modulo: 3 %}
    <div class="col-xl-4 col-md-6 mb-4">
      <div class="card border-0 shadow">{% if person.url %}<a href="{{ site.baseurl }}{{ person.url }}">{% endif %}
        <img src="{{ site.baseurl }}/assets/img/people/{{ person.image }}" class="card-img-top" alt="{{ person.name }}" style="object-fit: contain;">{% if person.url %}</a>{% endif %}
        <div class="card-body text-center">
          <h5 class="card-title mb-0">{{ person.name }}</h5>
          <div class="card-text text-black-50">{% if person.title %}{{ person.title }}{% else %}Research Software Engineer{% endif %}</div>
        </div>
      </div>
    </div>{% if loopindex == 0 %}</div><div class="row">{% endif %}
{% endfor %}
</div>
