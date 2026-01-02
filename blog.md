---
layout: page
title: Blog
permalink: /blog/
---
<style>
  blockquote {
    font-size: 16px !important;
    font-style: normal;
    color: #555;
  }
<style>
  /* 栏目大标题 */
  h3 {
    margin-top: 30px;
    margin-bottom: 10px;
    border-bottom: 2px solid #f0f0f0;
    padding-bottom: 5px;
  }
  
  /* 前三篇文章的列表样式 */
  .preview-list {
    margin-bottom: 10px;
    padding-left: 20px;
  }
  .preview-list li {
    margin-bottom: 6px;
  }

  /* 折叠条样式 */
  details {
    margin-bottom: 20px;
    background-color: #f9f9f9; /* 浅灰背景 */
    border-radius: 6px;
    border: 1px solid #eee;
  }
  
  summary {
    cursor: pointer;
    padding: 8px 15px;
    font-size: 0.9em;
    color: #555;
    font-weight: bold;
    user-select: none;
    outline: none;
  }
  
  summary:hover {
    background-color: #f0f0f0;
    color: #0366d6;
  }

  /* 折叠之后的内容区域 */
  .hidden-content {
    padding: 10px 15px 15px 15px;
    border-top: 1px solid #eee;
  }

  /* 引用块样式（藏在里面的简介） */
  .intro-quote {
    display: block;
    background-color: #fff;
    border-left: 4px solid #0366d6; /* 蓝色竖线 */
    padding: 10px 15px;
    color: #666;
    font-style: italic;
    font-size: 0.9em;
    margin-bottom: 15px;
  }
</style>

这是我的博客，展示各栏目 **最新 3 篇** 文章。点击底部按钮可查看栏目简介及历史归档。

---

### 鲲鹏之志篇

#### 1. 指挥部署
<ul class="preview-list">
  {% assign posts = site.categories['指挥部署'] %}
  {% for post in posts limit:3 %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
  {% else %}
    <li><span style="color:#ccc; font-size:0.9em;">(暂无最新文章)</span></li>
  {% endfor %}
</ul>

<details>
  <summary>查看简介 & 更多历史文章 ({{ posts.size | minus: 3 | at_least: 0 }}篇)...</summary>
  <div class="hidden-content">
    <div class="intro-quote">
      分享时事战略，一般很少更新，更多了号可能没了
    </div>
    <ul>
      {% for post in posts offset:3 %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
      {% else %}
        <li><span style="color:#ccc; font-size:0.9em;">没有更多历史文章了</span></li>
      {% endfor %}
    </ul>
  </div>
</details>


#### 2. 奇技淫巧
<ul class="preview-list">
  {% assign posts = site.categories['奇技淫巧'] %}
  {% for post in posts limit:3 %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
  {% else %}
    <li><span style="color:#ccc; font-size:0.9em;">(暂无最新文章)</span></li>
  {% endfor %}
</ul>

<details>
  <summary>查看简介 & 更多历史文章 ({{ posts.size | minus: 3 | at_least: 0 }}篇)...</summary>
  <div class="hidden-content">
    <div class="intro-quote">
      分享学习工具，各大专业通用
    </div>
    <ul>
      {% for post in posts offset:3 %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
      {% else %}
        <li><span style="color:#ccc; font-size:0.9em;">没有更多历史文章了</span></li>
      {% endfor %}
    </ul>
  </div>
</details>


#### 3. 念两句诗
<ul class="preview-list">
  {% assign posts = site.categories['念两句诗'] %}
  {% for post in posts limit:3 %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
  {% else %}
    <li><span style="color:#ccc; font-size:0.9em;">(暂无最新文章)</span></li>
  {% endfor %}
</ul>

<details>
  <summary>查看简介 & 更多历史文章 ({{ posts.size | minus: 3 | at_least: 0 }}篇)...</summary>
  <div class="hidden-content">
    <div class="intro-quote">
      分享古文诗词，看得懂就看，看不懂反思下自己是不是中国人
    </div>
    <ul>
      {% for post in posts offset:3 %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
      {% else %}
        <li><span style="color:#ccc; font-size:0.9em;">没有更多历史文章了</span></li>
      {% endfor %}
    </ul>
  </div>
</details>

---

### 口腹之欲篇

#### 4. 山水如画
<ul class="preview-list">
  {% assign posts = site.categories['山水如画'] %}
  {% for post in posts limit:3 %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
  {% else %}
    <li><span style="color:#ccc; font-size:0.9em;">(暂无最新文章)</span></li>
  {% endfor %}
</ul>

<details>
  <summary>查看简介 & 更多历史文章 ({{ posts.size | minus: 3 | at_least: 0 }}篇)...</summary>
  <div class="hidden-content">
    <div class="intro-quote">
      分享游记，起家篇目
    </div>
    <ul>
      {% for post in posts offset:3 %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
      {% else %}
        <li><span style="color:#ccc; font-size:0.9em;">没有更多历史文章了</span></li>
      {% endfor %}
    </ul>
  </div>
</details>


#### 5. 弄俩钱花
<ul class="preview-list">
  {% assign posts = site.categories['弄俩钱花'] %}
  {% for post in posts limit:3 %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
  {% else %}
    <li><span style="color:#ccc; font-size:0.9em;">(暂无最新文章)</span></li>
  {% endfor %}
</ul>

<details>
  <summary>查看简介 & 更多历史文章 ({{ posts.size | minus: 3 | at_least: 0 }}篇)...</summary>
  <div class="hidden-content">
    <div class="intro-quote">
      分享财经评论，不构成投资建议，市场有风险，投资需谨慎
    </div>
    <ul>
      {% for post in posts offset:3 %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
      {% else %}
        <li><span style="color:#ccc; font-size:0.9em;">没有更多历史文章了</span></li>
      {% endfor %}
    </ul>
  </div>
</details>


#### 6. 打猫踹狗
<ul class="preview-list">
  {% assign posts = site.categories['打猫踹狗'] %}
  {% for post in posts limit:3 %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
  {% else %}
    <li><span style="color:#ccc; font-size:0.9em;">(暂无最新文章)</span></li>
  {% endfor %}
</ul>

<details>
  <summary>查看简介 & 更多历史文章 ({{ posts.size | minus: 3 | at_least: 0 }}篇)...</summary>
  <div class="hidden-content">
    <div class="intro-quote">
      分享博主阴暗的内心，付费高级用户可解锁
    </div>
    <ul>
      {% for post in posts offset:3 %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
      {% else %}
        <li><span style="color:#ccc; font-size:0.9em;">没有更多历史文章了</span></li>
      {% endfor %}
    </ul>
  </div>
</details>
