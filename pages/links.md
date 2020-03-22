---
layout: page
title: Links
description: 友情鏈接
keywords: 友情鏈接
comments: true
menu: 聯接
permalink: /links/
---

> God made relatives. Thank God we can choose our friends.

{% for link in site.data.links %}
  {% if link.src == 'life' %}
* [{{ link.name }}]({{ link.url }})
  {% endif %}
{% endfor %}

> 友情鏈接

{% for link in site.data.links %}
  {% if link.src == 'friend' %}
* [{{ link.name }}]({{ link.url }})
  {% endif %}
{% endfor %}


{% for link in site.data.links %}
  {% if link.src == 'www' %}
* [{{ link.name }}]({{ link.url }})
  {% endif %}
{% endfor %}
