---
title: "Cryosphere Lab - Photos"
layout: piclay
excerpt: "Cryosphere Lab -- Photos"
permalink: /photos/
---

# Field Pictures

## Dadongshushan Pass in Qilian Mountain, Qinghai, 2018
By Jiahua Zhang
<div markdown="0" id="carousel" class="carousel slide" data-ride="carousel" data-interval="8000" data-pause="hover" >
<!-- Menu -->
<ol class="carousel-indicators">
<li data-target="#carousel" data-slide-to="0" class="active"></li>
<li data-target="#carousel" data-slide-to="1"></li>
<li data-target="#carousel" data-slide-to="2"></li>
</ol>

<!-- Items -->
<div class="carousel-inner" markdown="0">

<div class="item active">
<img src="{{ site.url }}{{ site.baseurl }}/images/field/Jiahua1.jpg" alt="Slide 1" />
</div>
<div class="item">
<img src="{{ site.url }}{{ site.baseurl }}/images/field/Jiahua2.jpg" alt="Slide 2" />
</div>
<div class="item">
<img src="{{ site.url }}{{ site.baseurl }}/images/field/Jiahua3.jpg" alt="Slide 3" />
</div>
</div>
<a class="left carousel-control" href="#carousel" role="button" data-slide="prev">
<span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
<span class="sr-only">Previous</span>
</a>
<a class="right carousel-control" href="#carousel" role="button" data-slide="next">
<span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
<span class="sr-only">Next</span>
</a>
</div>

## Rock glaciers in the European Alps, 2018
By Yan Hu
<div markdown="0" id="carousel" class="carousel slide" data-ride="carousel" data-interval="8000" data-pause="hover" >
    <!-- Menu -->
    <ol class="carousel-indicators">
        <li data-target="#carousel" data-slide-to="0" class="active"></li>
        <li data-target="#carousel" data-slide-to="1"></li>
        <li data-target="#carousel" data-slide-to="2"></li>
    </ol>

    <!-- Items -->
    <div class="carousel-inner" markdown="0">

        <div class="item active">
            <img src="{{ site.url }}{{ site.baseurl }}/images/field/yan_alps1.jpg" alt="Slide 1" />
        </div>
        <div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/field/yan_alps2.jpg" alt="Slide 2" />
        </div>
        <div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/field/yan_alps3.jpg" alt="Slide 3" />
        </div>
    </div>
  <a class="left carousel-control" href="#carousel" role="button" data-slide="prev">
    <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="right carousel-control" href="#carousel" role="button" data-slide="next">
    <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>


## Field Photos on the Tibetan Plateau, 2017-2018
By Lingcao Huang
<div markdown="0" id="carousel_lingcao" class="carousel slide" data-ride="carousel" data-interval="8000" data-pause="hover" >
    <!-- Menu -->
    <ol class="carousel-indicators">
        <li data-target="#carousel_lingcao" data-slide-to="0" class="active"></li>
        <li data-target="#carousel_lingcao" data-slide-to="1"></li>
        <li data-target="#carousel_lingcao" data-slide-to="2"></li>
        <li data-target="#carousel_lingcao" data-slide-to="3"></li>
        <li data-target="#carousel_lingcao" data-slide-to="4"></li>
    </ol>

    <!-- Items -->
    <div class="carousel-inner" markdown="0">

        <div class="item active">
            <img src="{{ site.url }}{{ site.baseurl }}/images/field/lingcao_thaw_slump2_beiluhe.jpg" alt="Slide 1" />
        </div>
        <div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/field/lingcao_thaw_slump1_beiluhe.jpg" alt="Slide 2" />
        </div>
        <div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/field/lingcao_thermal_erosion_gully_eboling.jpg" alt="Slide 3" />
        </div>
        <div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/field/lingcao_sinkhole_eobling.jpg" alt="Slide 4" />
        </div>
         <div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/field/lingcao_Hummocks2_maxianshan.jpg" alt="Slide 5" />
        </div>
    </div>
  <a class="left carousel-control" href="#carousel_lingcao" role="button" data-slide="prev">
    <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="right carousel-control" href="#carousel_lingcao" role="button" data-slide="next">
    <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>

## Old photos
(Right-click *'view image'* to see a larger image)
{% assign number_printed = 0 %}
{% for pic in site.data.field_pictures %}

{% assign even_odd = number_printed | modulo: 4 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-3 clearfix">
<img src="{{ site.url }}{{ site.baseurl }}/images/field/{{ pic.image }}" class="img-responsive" width="95%" style="float: left" />
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd > 2 %}
</div>
{% endif %}


{% endfor %}

{% assign even_odd = number_printed | modulo: 4 %}
{% if even_odd == 1 %}
</div>
{% endif %}

{% if even_odd == 2 %}
</div>
{% endif %}

{% if even_odd == 3 %}
</div>
{% endif %}

<p> &nbsp; </p>
