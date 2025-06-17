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
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/publication/{{ publi.image }}" class="img-responsive" width="66%" style="float: top" />
  <p> <em> {{ publi.description }} </em> </p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.highlight_display }}</a></strong></p>
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

<p> &nbsp; </p>


## List of Publications

<input type="text" id="searchInput" placeholder="Filter by topic or keyword..." style="margin-bottom: 1em; width: 100%; padding: 0.5em;">
<script>
document.addEventListener("DOMContentLoaded", function () {
  const input = document.getElementById("searchInput");
  input.addEventListener("keyup", function () {
    const filter = input.value.toLowerCase();
    const listItems = document.querySelectorAll(".pub-entry");
    listItems.forEach(function (item) {
      const text = item.textContent.toLowerCase();
      item.style.display = text.includes(filter) ? "" : "none";
    });
  });
});
</script>

<div id="pub-list">
{% for publi in site.data.publist %}
  <div class="pub-entry" style="margin-bottom: 1.5em;">
    <strong>{{ publi.title }}</strong><br />
    <em>{{ publi.authors }}</em><br />
    <a href="{{ publi.link.url }}"><strong>{{ publi.link.display }}</strong></a>
    {% if publi.incdata == 1 %}<br /><a href="{{ publi.dataurl }}">Data</a>{% endif %}
    {% if publi.inccode == 1 %}<br /><a href="{{ publi.code.url }}">{{ publi.code.display }}</a>{% endif %}
    <div style="display:none;">{{ publi.topic }}</div>
  </div>
{% endfor %}
</div>
