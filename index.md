---
layout: page
title: 狼煞的博客
tagline: 成功只有一个——按照自己的方式，去度过人生。
---
{% include JB/setup %}

## 日志列表:

<ul class="posts">
  {% for post in site.posts %}
    <li>
    	<span>
    		{{ post.date | date_to_string }}
    	</span>
    	&raquo;
    	<a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
    	<p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul>



