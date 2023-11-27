---
layout: default
title: Publications
nav_order: 4
permalink: /publications
last_modified_date: "now"
---

# Publications & Other Research Outputs
{: .fs-9 .no_toc }

[Google Scholar](https://scholar.google.com/citations?user=Zf0F0lIAAAAJ&hl=en&authuser=2){: .btn .btn-blue } 
[ResearchGate](https://www.researchgate.net/profile/Christopher-Keneally){: .btn .btn-primary}

------------------------------------------------------------------------

<details closed markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

------------------------------------------------------------------------

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
  <h3>{{ publi.title }}</h3>
  <p><em>{{ publi.description }}</em></p>
  <a href="{{ publi.link.url }}">
    <img src="{{ site.url }}{{ site.baseurl }}/assets/images/pubpic/{{ publi.image }}" class="img-responsive" width="100%" style="float: left; vertical-align: middle;" />
  </a>
  <p><em>{{ publi.authors }}</em>
  <strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
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

------------------------------------------------------------------------

## Full List of publications
&nbsp;
{% for publi in site.data.publist %}

<strong>  {{ publi.title }} </strong><br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}