---
title: "Cryosphere Lab - Team"
layout: gridlay
excerpt: "Cryosphere Lab: Team members"
sitemap: false
permalink: /team/
---

# Group Leader

{% assign number_printed = 0 %}
{% for member in site.data.team_lead %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-8 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/people/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br>email: <{{ member.email }}></i> 
  <br>
  <a href="https://www.ees.cuhk.edu.hk/staff/prof-liu-lin/"> Department Webpage </a>
  <br>
  <a href="{{ site.url }}{{ site.baseurl }}/assets/{{ member.cv }}"> CV </a> and  <a href="https://scholar.google.com.hk/citations?user=5VBaQTIAAAAJ&hl=en"> Google Scholar </a>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


# Group Members

{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-8 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/people/{{ member.photo }}" class="img-responsive" width="24%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br>email: <{{ member.email }}></i> {% if member.addcv == 1 %} <br><a href="{{ site.url }}{{ site.baseurl }}/assets/{{ member.cv }}"> CV </a> {% endif %}
  <p class="mb-0"> Research interests:</p>
  <ul style="overflow: hidden" padding-left="0em" margin-top="-10px">
  {% if member.number_intr == 1 %}
  <li> {{ member.interest1 }} </li>
  {% endif %}

  {% if member.number_intr == 2 %}
  <li> {{ member.interest1 }} </li>
  <li> {{ member.interest2 }} </li>
  {% endif %}

  {% if member.number_intr == 3 %}
  <li> {{ member.interest1 }} </li>
  <li> {{ member.interest2 }} </li>
  <li> {{ member.interest3 }} </li>
  {% endif %}

  {% if member.number_intr == 4 %}
  <li> {{ member.interest1 }} </li>
  <li> {{ member.interest2 }} </li>
  <li> {{ member.interest3 }} </li>
  <li> {{ member.interest4 }} </li>
  {% endif %}
  </ul>
  <br>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


 **We are looking for new PhD students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/openings) **!**

## Alumni
**Graduate Students**<br />
Xingyu (Carol) Xu, PhD and HKPFS recipient 2019-23, now Postdoc at CUHK <br />
Billy Ho Ming Tsang, MPhil 2020-22, now PhD student at University of Hong Kong <br />
Yan Hu, PhD and HKPFS recipient 2017-21, now Postdoc at University of Fribourg <br />
Jiahua Zhang, PhD 2017-21, now Project Scientist at University Corporation for Atmospheric Research (UCAR) <br />
Xiyu Xu, PhD 2015-21, now Researcher at Chongqing Forestry Research Institute <br />
Enze Zhang, PhD 2016-20, now Postdoc at Hong Kong University of Science and Technology <br />
Lingcao Huang, PhD 2016-19, now Research Assistant Professor at CUHK <br />
Jie Chen, PhD  2015-19 (co-supervised with Hui Lin), now Postdoc at University of Alaska Fairbanks <br />
Joseph Ma Ho Yin, MPhil 2014-16, later PhD at National University of Singapore, now Principal Scientist at Halliburton <br />

**Postdocs**<br />
Zhuoyi (Joey) Zhao, 2022-24, now Postdoc at University of Colorado Boulder  <br />
Xiaofan Zhu, 2022, now Associate Researcher at Northwest Institute of Eco-Environment and Resources, Chinese Academy of Sciences <br />
Guoyan Jiang, 2017-19, jointly supervised with Prof. T-f Wong, now Research Professor at Wuhan University <br />
Jiangjun Ran, 2018, now Associate Professor at Southern University of Science and Technology <br />
Bao Zhang, 2017-18, now Associate Professor at Wuhan University <br />
Zhiwei Zhou, 2017-18, now Associate Researcher at Innovation Academy for Precision Measurement Science and Technology, CAS <br />
Bo Hu, 2015, now faculty at Guangdong University of Technology <br />

**Research Assistants**<br />
Chengyan (Fancy) Fan, 2023-24, now PhD student at Lanzhou University <br />
Yufeng Hu, 2017-18, now Associate Professor at Chang'an University <br />
Kenneth Ho Ngai Lun, 2017-18, now Master Student at University of Southampton <br />
<a href="https://goimage.cn/">Xiaowen Wang</a>, 2016-17, now Associate Professor at Southwest Jiaotong University <br />

**Undergraduate Students (Final-year Project Advisees)**<br />
Yue Wu, 2017, later  PhD student at University of Texas at Austin <br />
Michelle Yip Man Wai, 2016, now PhD student at University of Hong Kong <br />

**Visiting Students**<br />
Mingkai Chen, 2023, now PhD student at Wuhan University <br />
Linyang Xin, 2019, now PhD student at Southern University of Science and Technology <br />
Yidan Ding and Haoran Wang, 2019, master students at Jilin University <br />
Weifan Zhou, 2018, master student at Jilin University <br />
Zhenming Wu, 2017, later PhD student at Reading University <br />
Jiahui Wang, 2017, later PhD at Southern Methodist University <br />
Yongxin Liu, 2017, undergraduate student at Wuhan University <br />
Wanwan Shao, 2016-17, PhD at Lanzhou University <br />
Weiyu Zheng, 2015, later PhD at Southern Methodist University <br />
