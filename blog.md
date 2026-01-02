---
layout: page
title: My Blog
permalink: /blog/
---
这是我的博客，根据内容性质划分为 2 篇 6 个主要栏目：

---

### 鲲鹏之志篇

#### 1. 指挥部署

> 分享时事战略，一般很少更新，更多了号可能没了

<ul>
  {% for post in site.categories['指挥部署'] %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#888;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
  {% endfor %}
</ul>

#### 2. 奇技淫巧

> 分享学习工具，各大专业通用

<ul>
  {% for post in site.categories['奇技淫巧'] %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#888;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
  {% endfor %}
</ul>

#### 3. 念两句诗

> 分享古文诗词，看得懂就看，看不懂反思下自己是不是中国人

<ul>
  {% for post in site.categories['念两句诗'] %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#888;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
  {% endfor %}
</ul>

---

### 口腹之欲篇

#### 4. 山水如画

> 分享游记，起家篇目

<ul>
  {% for post in site.categories['山水如画'] %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#888;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
  {% endfor %}
</ul>

#### 5. 弄俩钱花

> 分享财经评论，不构成投资建议，市场有风险，投资需谨慎

<ul>
  {% for post in site.categories['弄俩钱花'] %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#888;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
  {% endfor %}
</ul>

#### 6. 打猫踹狗

> 分享博主阴暗的内心，付费高级用户可解锁

<ul>
  {% for post in site.categories['打猫踹狗'] %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#888;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
  {% endfor %}
</ul>
