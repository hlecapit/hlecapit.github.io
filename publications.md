---
layout: article
titles:
  # @start locale config
  en      : &EN      Publications
  en-GB   : *EN
  en-US   : *EN
  en-CA   : *EN
  en-AU   : *EN
  fr      : &FR       Publications
  fr-BE   : *FR
  fr-CA   : *FR
  fr-CH   : *FR
  fr-FR   : *FR
  fr-LU   : *FR
  # @end locale config
key: page-pubs
---
Starting from 2020, you can also check my [Hal profile](https://hal.science/search/index/q/*/authIdHal_s/hoel-le-capitaine) and my [Google Scholar profile](https://scholar.google.com/citations?user=JadlFKYAAAAJ&hl=en) for older publications.
<ul>
{% assign publications = site.publications | sort: "year" | reverse %}
{% for pub in publications %}
<li>
<div class="pubitem">
  <div class="pubtitle">{{ pub.title }}</div>
  <div class="pubauthors">{{ pub.authors }}</div>
  <div class="pubinfo">{{ pub.publication }}, {{ pub.year}}</div>
  <div class="publink"> <a href="{{pub.doi}}"><i class="far fa-file-pdf"></i> Paper </a><a href="{{pub.doi}}"><i class="far fa-file-code"></i> Code</a></div>
</div>
</li>
{% endfor %}
</ul>