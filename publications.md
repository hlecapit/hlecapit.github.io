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
(starting from 2012)
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