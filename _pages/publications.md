---
title: "Schäberle Lab - Publications"
layout: gridlay
excerpt: "Schäberle Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Group highlights

**At the end of this page, you can find the [full list of publications and patents](#full-list-of-publications). All papers are also available on [arXiv](https://arxiv.org/search/?searchtype=author&query=Allan%2C+M+P).**

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
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
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

## Full List of publications

{% assign pubs_by_year = site.data.publist | group_by: "year" | sort: "name" | reverse %}
{% assign counter = site.data.publist | size %}

{% for year in pubs_by_year %}
<h3>{{ year.name }}</h3>
<ul style="list-style: none; padding-left: 0;">
  {% for publi in year.items %}
    <li style="margin-bottom: 1rem;">
      <span style="font-weight:700;">[{{ counter }}]</span> {{ publi.authors }}<br>
      <strong><a href="{{ publi.link.url }}">{{ publi.title }}</a></strong><br>
      {{ publi.link.display }}
    </li>
    {% assign counter = counter | minus: 1 %}
  {% endfor %}
</ul>
{% endfor %}
