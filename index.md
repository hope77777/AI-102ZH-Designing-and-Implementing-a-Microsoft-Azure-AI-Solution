---
title: 在线托管的说明
permalink: index.html
layout: home
---

# 内容目录

以下列出了每个实验室练习和演示的超链接。

## 实验室

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions'" %}
| 模块 | 实验室 |
| --- | --- | 
{% for activity in labs  %}| {{ activity.lab.module }} | [{{ activity.lab.title }}{% if activity.lab.type %} - {{ activity.lab.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

