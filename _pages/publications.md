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

<!-- Search and Topic Filter UI -->
<input type="text" id="searchInput" placeholder="Search title, author, or topic..." style="margin-bottom: 1em; width: 100%; padding: 0.5em;" />

<label for="topicFilter"><strong>Filter by Topic:</strong></label>
<select id="topicFilter" style="margin-bottom: 1.5em; width: 100%; padding: 0.5em;">
  <option value="">All Topics</option>
  <option value="Cryosphere">Cryosphere</option>
  <option value="Remote Sensing">Remote Sensing</option>
  <option value="InSAR">InSAR</option>
  <option value="Permafrost">Permafrost</option>
</select>

<script>
document.addEventListener("DOMContentLoaded", function () {
  const input = document.getElementById("searchInput");
  const topicFilter = document.getElementById("topicFilter");

  function applyFilters() {
    const keyword = input.value.toLowerCase();
    const selectedTopic = topicFilter.value;

    document.querySelectorAll(".pub-entry").forEach(function (item) {
      const text = item.textContent.toLowerCase();
      const topic = item.getAttribute("data-topic");

      const matchesKeyword = text.includes(keyword);
      const matchesTopic = !selectedTopic || topic === selectedTopic;

      item.style.display = matchesKeyword && matchesTopic ? "" : "none";
    });
  }

  input.addEventListener("input", applyFilters);
  topicFilter.addEventListener("change", applyFilters);
});
</script>

<!-- Publications List -->
<div id="pub-list">
  {% for publi in site.data.publist %}
    <div class="pub-entry" data-topic="{{ publi.topic | escape }}" style="margin-bottom: 1.5em; padding-bottom: 1em; border-bottom: 1px solid #ddd;">
      <strong>{{ publi.title }}</strong><br />
      <em>{{ publi.authors }}</em><br />
      <a href="{{ publi.link.url }}"><strong>{{ publi.link.display }}</strong></a>
      {% if publi.incdata == 1 %}<br /><a href="{{ publi.dataurl }}">Data</a>{% endif %}
      {% if publi.inccode == 1 %}<br /><a href="{{ publi.code.url }}">{{ publi.code.display }}</a>{% endif %}
      <br /><span style="font-style: italic; color: #666;">Topic: {{ publi.topic }}</span>
    </div>
  {% endfor %}
</div>

