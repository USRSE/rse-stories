---
layout: wide
title: Phenotypes
description: A collection of shared phenotypes!
permalink: /phenotypes/
---

{% include scrolltop.html %}

The RSE Phenotype is a simple plot to show the dimensions that help to define work, and the communities served for a particular research software engineer. They are generated using the <a href="https://rseng.github.io/rse-phenotype/" target="_blank">RSE Phenotype Generator</a>
Below is a spattering of phenotypes you can explore, for your interest.<br>

<div class="row" style="margin:25px; padding:30px">
   {% for post in site.posts %}{% if post.phenotype %}
    <a href="{{ site.baseurl }}/assets/img/phenotypes/{{ post.phenotype }}"><img src="{{ site.baseurl }}/assets/img/phenotypes/{{ post.phenotype }}" loading="lazy"></a>{% endif %}
   {% endfor %}
</div>
