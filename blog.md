---
layout: page
title: Blog
permalink: /blog/
---

<style>
  /* --- 整体容器样式 --- */
  details {
    margin-bottom: 20px;
    background: #fff;
    border: 1px solid #e1e4e8;
    border-radius: 8px;
    box-shadow: 0 1px 3px rgba(0,0,0,0.05);
    transition: all 0.2s ease;
  }
  details[open] {
    box-shadow: 0 4px 10px rgba(0,0,0,0.1); /* 展开时阴影加深 */
  }

  /* --- 标题栏(Summary) = 标题 + 最新3篇 --- */
  summary {
    cursor: pointer;
    padding: 15px 20px;
    outline: none;
    list-style: none; /* 隐藏默认小三角 */
    position: relative;
  }
  /* 隐藏Webkit浏览器的小三角 */
  summary::-webkit-details-marker { display: none; }

  /* 栏目标题设计 */
  .category-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 10px; /* 标题和预览文章的间距 */
  }
  .category-title {
    font-size: 1.3em;
    font-weight: bold;
    color: #24292e;
  }
  .post-count {
    background: #f1f8ff;
    color: #0366d6;
    padding: 2px 10px;
    border-radius: 12px;
    font-size: 0.8em;
    font-weight: bold;
  }

  /* --- 预览列表 (最新3篇) --- */
  .preview-list {
    margin: 0;
    padding-left: 5px; /*稍微缩进一点*/
    list-style: none;
  }
  .preview-list li {
    padding: 3px 0;
    font-size: 1em;
    border-left: 2px solid transparent; /* 占位，为了和展开后的对齐 */
  }
  /* 鼠标悬停在Summary整体时，提示可点击 */
  summary:hover .category-title {
    color: #0366d6;
    text-decoration: underline;
  }

  /* --- 展开后的区域 (简介 + 剩余文章) --- */
  .expanded-content {
    padding: 0 20px 20px 20px;
    border-top: 1px dashed #e1e4e8; /* 虚线分割预览和历史 */
    margin-top: -5px;
    animation: slideDown 0.3s ease-out;
  }

  /* 简介块 */
  .intro-quote {
    margin: 15px 0;
    padding: 10px 15px;
    background-color: #f6f8fa;
    border-left: 4px solid #0366d6;
    color: #586069;
    font-style: italic;
    font-size: 0.9em;
  }

  /* 历史文章列表 */
  .archive-list {
    margin: 0;
    padding-left: 5px;
    list-style: none;
  }
  .archive-list li {
    padding: 3px 0;
    color: #666;
  }

  /* 简单的展开动画 */
  @keyframes slideDown {
    from { opacity: 0; transform: translateY(-10px); }
    to { opacity: 1; transform: translateY(0); }
  }
  
  /* 链接样式 */
  a { text-decoration: none; color: #24292e; }
  a:hover { color: #0366d6; }
  .date-tag { font-size: 0.8em; color: #999; margin-left: 5px; }
</style>
---

### 鲲鹏之志篇

<details>
  <summary>
    <div class="category-header">
      <span class="category-title">1. 指挥部署</span>
      <span class="post-count">{{ site.categories['指挥部署'].size | default: 0 }} 篇</span>
    </div>
    <ul class="preview-list">
      {% for post in site.categories['指挥部署'] limit:3 %}
        <li>🔹 <a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
      {% else %}
        <li style="color:#ccc;">(暂无文章)</li>
      {% endfor %}
    </ul>
  </summary>
  
  <div class="expanded-content">
    <div class="intro-quote">这里是简介：分享时事战略，一般很少更新，更多了号可能没了</div>
    <ul class="archive-list">
      {% for post in site.categories['指挥部署'] offset:3 %}
        <li>🔸 <a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
      {% else %}
        <li style="color:#ccc; font-size:0.9em; padding-top:10px;">没有更多历史文章了...</li>
      {% endfor %}
    </ul>
  </div>
</details>

<details>
  <summary>
    <div class="category-header">
      <span class="category-title">2. 奇技淫巧</span>
      <span class="post-count">{{ site.categories['奇技淫巧'].size | default: 0 }} 篇</span>
    </div>
    <ul class="preview-list">
      {% for post in site.categories['奇技淫巧'] limit:3 %}
        <li>🔹 <a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
      {% else %}
        <li style="color:#ccc;">(暂无文章)</li>
      {% endfor %}
    </ul>
  </summary>
  <div class="expanded-content">
    <div class="intro-quote">这里是简介：分享学习工具，各大专业通用</div>
    <ul class="archive-list">
      {% for post in site.categories['奇技淫巧'] offset:3 %}
        <li>🔸 <a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
      {% endfor %}
    </ul>
  </div>
</details>

<details>
  <summary>
    <div class="category-header">
      <span class="category-title">3. 念两句诗</span>
      <span class="post-count">{{ site.categories['念两句诗'].size | default: 0 }} 篇</span>
    </div>
    <ul class="preview-list">
      {% for post in site.categories['念两句诗'] limit:3 %}
        <li>🔹 <a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
      {% else %}
        <li style="color:#ccc;">(暂无文章)</li>
      {% endfor %}
    </ul>
  </summary>
  <div class="expanded-content">
    <div class="intro-quote">这里是简介：分享古文诗词，看得懂就看，看不懂反思下自己是不是中国人</div>
    <ul class="archive-list">
      {% for post in site.categories['念两句诗'] offset:3 %}
        <li>🔸 <a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
      {% endfor %}
    </ul>
  </div>
</details>

---

### 口腹之欲篇

<details open> <summary>
    <div class="category-header">
      <span class="category-title">4. 山水如画 (默认展开演示)</span>
      <span class="post-count">{{ site.categories['山水如画'].size | default: 0 }} 篇</span>
    </div>
    <ul class="preview-list">
      {% for post in site.categories['山水如画'] limit:3 %}
        <li>🔹 <a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
      {% else %}
        <li style="color:#ccc;">(暂无文章)</li>
      {% endfor %}
    </ul>
  </summary>
  <div class="expanded-content">
    <div class="intro-quote">这里是简介：分享游记，起家篇目</div>
    <ul class="archive-list">
      {% for post in site.categories['山水如画'] offset:3 %}
        <li>🔸 <a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
      {% endfor %}
    </ul>
  </div>
</details>

<details>
  <summary>
    <div class="category-header">
      <span class="category-title">5. 弄俩钱花</span>
      <span class="post-count">{{ site.categories['弄俩钱花'].size | default: 0 }} 篇</span>
    </div>
    <ul class="preview-list">
      {% for post in site.categories['弄俩钱花'] limit:3 %}
        <li>🔹 <a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
      {% endfor %}
    </ul>
  </summary>
  <div class="expanded-content">
    <div class="intro-quote">这里是简介：分享财经评论，不构成投资建议，市场有风险，投资需谨慎</div>
    <ul class="archive-list">
      {% for post in site.categories['弄俩钱花'] offset:3 %}
        <li>🔸 <a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
      {% endfor %}
    </ul>
  </div>
</details>

<details>
  <summary>
    <div class="category-header">
      <span class="category-title">6. 打猫踹狗</span>
      <span class="post-count">{{ site.categories['打猫踹狗'].size | default: 0 }} 篇</span>
    </div>
    <ul class="preview-list">
      {% for post in site.categories['打猫踹狗'] limit:3 %}
        <li>🔹 <a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
      {% else %}
        <li style="color:#ccc;">(暂无文章)</li>
      {% endfor %}
    </ul>
  </summary>
  <div class="expanded-content">
    <div class="intro-quote">这里是简介：分享博主阴暗的内心，付费高级用户可解锁</div>
    <ul class="archive-list">
      {% for post in site.categories['打猫踹狗'] offset:3 %}
        <li>🔸 <a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
      {% endfor %}
    </ul>
  </div>
</details>
