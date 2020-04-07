---
layout: categories
title: Categories
description: 哈哈，你找到了我的文章基因库
keywords: 分类
comments: false
menu: 分类
permalink: /categories/
---

<section class="container posts-content">
{% assign sorted_categories = site.categories | sort %}
{% for category in sorted_categories %}
	{% assign wordCountSum = 0 %}
	{% for post in category.last %}
		{% assign wordCount = post.content | strip_html | strip_newlines | size %}
		{% assign wordCountSum = wordCountSum | plus: wordCount %}
	{% endfor %}
	<h3 id="{{ category[0] }}">{{ category | first }} {{ wordCountSum }} 字/Words</h3>
	<ol class="posts-list">
	{% for post in category.last %}
	<li class="posts-list-item">
	<span class="posts-list-meta">{{ post.date | date:"%Y-%m-%d" }}</span>
	<a class="posts-list-name" href="{{ site.url }}{{ post.url }}">{{ post.title }}</a>
	</li>
{% endfor %}
</ol>
{% endfor %}
</section>
<!-- /section.content -->
