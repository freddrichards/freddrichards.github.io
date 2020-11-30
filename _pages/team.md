---
title: "Fred Richards - Team"
layout: gridlay
excerpt: "Fred Richards - Team"
sitemap: false
permalink: /team/
---

<h3 style="font-weight: bold">Group members</h3> 

<h3 style="font-weight: bold">Current:</h3>
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="27%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br>email: <{{ member.email }}></i>
  <ul style="overflow: hidden">

  {% if member.number_addit == 1 %}
  <li> {{ member.addit1 }} </li>
  {% endif %}

  {% if member.number_addit == 2 %}
  <li> {{ member.addit1 }} </li>
  <li> {{ member.addit2 }} </li>
  {% endif %}

  </ul>
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

[comment]: <> (<h3 style="font-weight: bold">Openings:</h3>)

[comment]: <> (<i>Ph.D. studentships available for Spring 2021. See [here](https://graduate.rsmas.miami.edu/_assets/pdf/phd-assistanships/advert-fall2021.pdf) and [here](https://www.graduate.rsmas.miami.edu/admissions/phd-assistanships/index.html) for more details and get in touch if interested!</i>)

<br>
<br>
