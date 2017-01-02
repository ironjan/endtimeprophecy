---
title: Shows
date: 2016-12-31T00:00:00+00:00
author: Jan
layout: page
---

{% for show in site.data.shows %}

{% assign year  = show.date | date: '%Y' %}
{% assign month = show.date | date: '%m' %}
{% assign day   = show.date | date: '%d' %}

<div class="show">
<h2>{{show.title}} @ {{show.date}} - {{ show.date | date: '%B %d, %Y' }} </h2>

{% if show.url %}
  <a href="{{show.url}}">{{show.url}}</a>
{% endif %}

<!--
{% if show.image %}
<img src="/images/{{year}}/{{month}}/{{day}}/{{show.image}}" />
{% endif %}
-->

{{show}}




</div>
{% endfor %}