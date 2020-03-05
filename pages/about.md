---
layout: page
title: About
description: A simple blog
keywords: White Rice, blog
comments: true
menu: About/关于
permalink: /about/
---

I'm White Rice Porridge. This is a simple blog.

## 联系/Contact

{% for website in site.data.social %}
* {{ website.sitename }}：[@{{ website.name }}]({{ website.url }})
{% endfor %}

## Skill Keywords

{% for category in site.data.skills %}
### {{ category.name }}
<div class="btn-inline">
{% for keyword in category.keywords %}
<button class="btn btn-outline" type="button">{{ keyword }}</button>
{% endfor %}
</div>
{% endfor %}
