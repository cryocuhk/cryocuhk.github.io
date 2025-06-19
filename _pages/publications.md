---
title: "Cryosphere Lab - Publications"
layout: gridlay
excerpt: "Cryosphere Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications
For a full list see [below](#list-of-publications) or go to [Google Scholar](https://scholar.google.com.hk/citations?user=5VBaQTIAAAAJ&hl=en)

## Highlights

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <strong>{{ publi.title }}</strong>
  <img src="{{ site.url }}{{ site.baseurl }}/images/publication/{{ publi.image }}" class="img-responsive" width="66%" style="float: top" />
  {% if publi.description %}
  <p><em>{{ publi.description }}</em></p>
  {% endif %}
  {% if publi.link and publi.highlight_display %}
  <p><strong><a href="{{ publi.link.url }}">{{ publi.highlight_display | default: publi.title }}</a></strong></p>
  {% endif %}
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<div class="my-3"></div>


## List of Publications

The sorting by topic function is under development. The current version causes some misformating in the list below.

{% for publi in site.data.publist %}

  **{{ publi.title }}** <br />
  <em>{{ publi.authors }} </em><br />
  <a href="{{ publi.link.url }}"><strong>{{ publi.link.display }}</strong></a>
  {% if publi.incdata == 1 %} <br/><a href="{{ publi.dataurl }}">Data</a> {% endif %} 
  {% if publi.inccode == 1 %} <br/><a href="{{ publi.code.url }}">{{ publi.code.display }}</a> {% endif %} 

{% endfor %}

