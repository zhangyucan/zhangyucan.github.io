---
layout: page
title: Blog
permalink: /blog/
---
<style>
  /* --- 容器样式 --- */
  details {
    margin-bottom: 20px;
    background: #fff;
    border: 1px solid #e1e4e8;
    border-radius: 8px;
    /* 默认状态下不需要阴影，展开后再加 */
    transition: all 0.2s;
  }
  
  /* --- 核心交互逻辑（魔法所在） --- */
  
  /* 1. 当折叠框展开(open)时，把 summary 里的“预览列表”隐藏掉 */
  details[open] summary .preview-container {
    display: none;
  }
  
  /* 2. 展开时给整体加个阴影，更有沉浸感 */
  details[open] {
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    border-color: #0366d6;
  }

  /* --- 标题栏 (Summary) --- */
  summary {
    cursor: pointer;
    padding: 15px 20px;
    outline: none;
    list-style: none;
    position: relative;
  }
  summary::-webkit-details-marker { display: none; }

  /* 标题行布局 */
  .header-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 1.2em;
    font-weight: bold;
    color: #24292e;
    margin-bottom: 8px;
  }
  
  /* 鼠标悬停标题变色 */
  summary:hover .header-row {
    color: #0366d6;
  }

  /* 文章篇数小胶囊 */
  .badge {
    font-size: 0.6em;
    background: #f1f8ff;
    color: #0366d6;
    padding: 2px 8px;
    border-radius: 10px;
    vertical-align: middle;
  }

  /* --- 预览列表 (默认展示的部分) --- */
  .preview-container {
    padding-left: 5px;
    animation: fadeIn 0.5s;
  }
  .preview-item {
    font-size: 0.95em;
    color: #555;
    margin-bottom: 5px;
    padding-left: 10px;
    border-left: 2px solid #e1e4e8; /* 灰色竖线 */
  }
  .preview-tips {
    font-size: 0.8em;
    color: #aaa;
    margin-top: 8px;
    font-style: italic;
  }

  /* --- 完整内容 (点开后展示的部分) --- */
  .full-content {
    padding: 0 20px 20px 20px;
    border-top: 1px solid #eaecef;
    animation: slideDown 0.3s ease-out;
  }

  /* 简介引用块 */
  .intro-block {
    margin: 15px 0 20px 0;
    padding: 10px 15px;
    background-color: #f6f8fa;
    border-left: 4px solid #0366d6; /* 蓝色竖线 */
    color: #586069;
    font-style: italic;
  }

  /* 全部文章列表 */
  .all-posts-list {
    list-style: none;
    padding-left: 5px;
    margin: 0;
  }
  .all-posts-list li {
    padding: 8px 0;
    border-bottom: 1px dashed #eee;
    font-size: 1em;
  }
  .all-posts-list li:last-child { border-bottom: none; }

  /* 辅助动画 */
  @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
  @keyframes slideDown { from { opacity: 0; transform: translateY(-5px); } to { opacity: 1; transform: translateY(0); } }

  /* 链接通用 */
  a { text-decoration: none; color: #24292e; }
  a:hover { color: #0366d6; text-decoration: underline; }
  .date { float: right; font-size: 0.85em; color: #999; }
</style>

这是我的博客，默认展示各栏目 **最新 3 篇预览**。点击栏目即可切换至 **完整模式**。

---

### 鲲鹏之志篇

<details>
  <summary>
    <div class="header-row">
      <span>1. 指挥部署 <span class="badge">{{ site.categories['指挥部署'].size | default: 0 }}</span></span>
      <span style="font-size:0.8em; color:#ccc;">▼</span>
    </div>
    <div class="preview-container">
      {% for post in site.categories['指挥部署'] limit:3 %}
        <div class="preview-item">
          <a href="{{ post.url }}">{{ post.title }}</a>
        </div>
      {% else %}
        <div class="preview-item" style="color:#ccc;">(暂无文章)</div>
      {% endfor %}
      {% if site.categories['指挥部署'].size > 0 %}
        <div class="preview-tips">... 点击展开查看完整列表及简介</div>
      {% endif %}
    </div>
  </summary>

  <div class="full-content">
    <div class="intro-block">
      分享时事战略，一般很少更新，更多了号可能没了
    </div>
    <ul class="all-posts-list">
      {% for post in site.categories['指挥部署'] %}
        <li>
          <a href="{{ post.url }}">{{ post.title }}</a>
          <span class="date">{{ post.date | date: "%Y-%m-%d" }}</span>
        </li>
      {% else %}
        <li style="color:#ccc;">暂无文章</li>
      {% endfor %}
    </ul>
  </div>
</details>

<details>
  <summary>
    <div class="header-row">
      <span>2. 奇技淫巧 <span class="badge">{{ site.categories['奇技淫巧'].size | default: 0 }}</span></span>
      <span style="font-size:0.8em; color:#ccc;">▼</span>
    </div>
    <div class="preview-container">
      {% for post in site.categories['奇技淫巧'] limit:3 %}
        <div class="preview-item">
          <a href="{{ post.url }}">{{ post.title }}</a>
        </div>
      {% else %}
        <div class="preview-item" style="color:#ccc;">(暂无文章)</div>
      {% endfor %}
      {% if site.categories['奇技淫巧'].size > 0 %}
        <div class="preview-tips">... 点击展开查看完整列表及简介</div>
      {% endif %}
    </div>
  </summary>

  <div class="full-content">
    <div class="intro-block">
      分享学习工具，各大专业通用
    </div>
    <ul class="all-posts-list">
      {% for post in site.categories['奇技淫巧'] %}
        <li>
          <a href="{{ post.url }}">{{ post.title }}</a>
          <span class="date">{{ post.date | date: "%Y-%m-%d" }}</span>
        </li>
      {% endfor %}
    </ul>
  </div>
</details>

<details>
  <summary>
    <div class="header-row">
      <span>3. 念两句诗 <span class="badge">{{ site.categories['念两句诗'].size | default: 0 }}</span></span>
      <span style="font-size:0.8em; color:#ccc;">▼</span>
    </div>
    <div class="preview-container">
      {% for post in site.categories['念两句诗'] limit:3 %}
        <div class="preview-item">
          <a href="{{ post.url }}">{{ post.title }}</a>
        </div>
      {% else %}
        <div class="preview-item" style="color:#ccc;">(暂无文章)</div>
      {% endfor %}
      {% if site.categories['念两句诗'].size > 0 %}
        <div class="preview-tips">... 点击展开查看完整列表及简介</div>
      {% endif %}
    </div>
  </summary>

  <div class="full-content">
    <div class="intro-block">
      分享古文诗词，看得懂就看，看不懂反思下自己是不是中国人
    </div>
    <ul class="all-posts-list">
      {% for post in site.categories['念两句诗'] %}
        <li>
          <a href="{{ post.url }}">{{ post.title }}</a>
          <span class="date">{{ post.date | date: "%Y-%m-%d" }}</span>
        </li>
      {% endfor %}
    </ul>
  </div>
</details>

---

### 口腹之欲篇

<details>
  <summary>
    <div class="header-row">
      <span>4. 山水如画 <span class="badge">{{ site.categories['山水如画'].size | default: 0 }}</span></span>
      <span style="font-size:0.8em; color:#ccc;">▼</span>
    </div>
    <div class="preview-container">
      {% for post in site.categories['山水如画'] limit:3 %}
        <div class="preview-item">
          <a href="{{ post.url }}">{{ post.title }}</a>
        </div>
      {% else %}
        <div class="preview-item" style="color:#ccc;">(暂无文章)</div>
      {% endfor %}
      {% if site.categories['山水如画'].size > 0 %}
        <div class="preview-tips">... 点击展开查看完整列表及简介</div>
      {% endif %}
    </div>
  </summary>

  <div class="full-content">
    <div class="intro-block">
      分享游记，起家篇目
    </div>
    <ul class="all-posts-list">
      {% for post in site.categories['山水如画'] %}
        <li>
          <a href="{{ post.url }}">{{ post.title }}</a>
          <span class="date">{{ post.date | date: "%Y-%m-%d" }}</span>
        </li>
      {% endfor %}
    </ul>
  </div>
</details>

<details>
  <summary>
    <div class="header-row">
      <span>5. 弄俩钱花 <span class="badge">{{ site.categories['弄俩钱花'].size | default: 0 }}</span></span>
      <span style="font-size:0.8em; color:#ccc;">▼</span>
    </div>
    <div class="preview-container">
      {% for post in site.categories['弄俩钱花'] limit:3 %}
        <div class="preview-item">
          <a href="{{ post.url }}">{{ post.title }}</a>
        </div>
      {% else %}
        <div class="preview-item" style="color:#ccc;">(暂无文章)</div>
      {% endfor %}
      {% if site.categories['弄俩钱花'].size > 0 %}
        <div class="preview-tips">... 点击展开查看完整列表及简介</div>
      {% endif %}
    </div>
  </summary>

  <div class="full-content">
    <div class="intro-block">
      分享财经评论，不构成投资建议，市场有风险，投资需谨慎
    </div>
    <ul class="all-posts-list">
      {% for post in site.categories['弄俩钱花'] %}
        <li>
          <a href="{{ post.url }}">{{ post.title }}</a>
          <span class="date">{{ post.date | date: "%Y-%m-%d" }}</span>
        </li>
      {% endfor %}
    </ul>
  </div>
</details>

<details>
  <summary>
    <div class="header-row">
      <span>6. 打猫踹狗 <span class="badge">{{ site.categories['打猫踹狗'].size | default: 0 }}</span></span>
      <span style="font-size:0.8em; color:#ccc;">▼</span>
    </div>
    <div class="preview-container">
      {% for post in site.categories['打猫踹狗'] limit:3 %}
        <div class="preview-item">
          <a href="{{ post.url }}">{{ post.title }}</a>
        </div>
      {% else %}
        <div class="preview-item" style="color:#ccc;">(暂无文章)</div>
      {% endfor %}
      {% if site.categories['打猫踹狗'].size > 0 %}
        <div class="preview-tips">... 点击展开查看完整列表及简介</div>
      {% endif %}
    </div>
  </summary>

  <div class="full-content">
    <div class="intro-block">
      分享博主阴暗的内心，付费高级用户可解锁
    </div>
    <ul class="all-posts-list">
      {% for post in site.categories['打猫踹狗'] %}
        <li>
          <a href="{{ post.url }}">{{ post.title }}</a>
          <span class="date">{{ post.date | date: "%Y-%m-%d" }}</span>
        </li>
      {% endfor %}
    </ul>
  </div>
</details>
