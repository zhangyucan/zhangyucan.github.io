---
layout: page
title: Blog
permalink: /blog/
---
<style>
  /* --- 整体容器 --- */
  details {
    margin-bottom: 15px;
    background: #fff;
    border: 1px solid #e1e4e8;
    border-radius: 6px;
    transition: all 0.2s;
  }
  /* 悬停时加一点阴影，更有质感 */
  details:hover {
    box-shadow: 0 2px 8px rgba(0,0,0,0.05);
    border-color: #d1d5da;
  }
  details[open] {
    border-left: 4px solid #0366d6; /* 展开时左边变蓝 */
  }

  /* --- 标题栏 (Summary) --- */
  summary {
    cursor: pointer;
    padding: 15px 20px;
    outline: none;
    list-style: none; /* 隐藏默认小三角 */
    display: flex;
    justify-content: space-between; /* 左右两端对齐 */
    align-items: center;
  }
  summary::-webkit-details-marker { display: none; }

  /* 标题文字 */
  .category-title {
    font-size: 1.1em;
    font-weight: bold;
    color: #24292e;
  }
  /* 数量胶囊 */
  .post-count {
    background: #f1f8ff;
    color: #0366d6;
    padding: 2px 10px;
    border-radius: 12px;
    font-size: 0.8em;
    font-weight: bold;
  }

  /* --- 展开后的内容区域 --- */
  .expanded-content {
    padding: 0 20px 20px 20px;
    border-top: 1px solid #eaecef;
    animation: fadeIn 0.3s ease;
  }

  /* 简介块 */
  .intro-quote {
    margin: 15px 0;
    padding: 10px 15px;
    background-color: #f6f8fa;
    color: #586069;
    font-style: italic;
    font-size: 0.9em;
    border-radius: 4px;
  }

  /* --- 文章列表样式 --- */
  .section-label {
    font-size: 0.85em;
    color: #999;
    margin: 15px 0 5px 0;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
  }
  
  ul.clean-list {
    margin: 0;
    padding-left: 10px;
    list-style: none;
  }
  ul.clean-list li {
    padding: 5px 0;
    border-bottom: 1px dashed #f0f0f0;
  }
  ul.clean-list li:last-child {
    border-bottom: none;
  }
  
  a { text-decoration: none; color: #24292e; }
  a:hover { color: #0366d6; text-decoration: underline; }
  .date-tag { font-size: 0.8em; color: #bbb; margin-left: 8px; float: right;}

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(-5px); }
    to { opacity: 1; transform: translateY(0); }
  }
</style>

这是我的博客，共包含 **2篇6个** 主要栏目。点击标题展开查看详情。

---

### 鲲鹏之志篇

<details>
  <summary>
    <span class="category-title">1. 指挥部署</span>
    <span class="post-count">{{ site.categories['指挥部署'].size | default: 0 }}</span>
  </summary>
  <div class="expanded-content">
    <div class="intro-quote">简介：分享时事战略，一般很少更新，更多了号可能没了</div>
    
    <div class="section-label">🆕 最新发布</div>
    <ul class="clean-list">
      {% for post in site.categories['指挥部署'] limit:3 %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
      {% else %}
        <li style="color:#ccc;">暂无文章</li>
      {% endfor %}
    </ul>

    {% if site.categories['指挥部署'].size > 3 %}
      <div class="section-label">🗄️ 历史归档</div>
      <ul class="clean-list">
        {% for post in site.categories['指挥部署'] offset:3 %}
          <li><a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
        {% endfor %}
      </ul>
    {% endif %}
  </div>
</details>


<details>
  <summary>
    <span class="category-title">2. 奇技淫巧</span>
    <span class="post-count">{{ site.categories['奇技淫巧'].size | default: 0 }}</span>
  </summary>
  <div class="expanded-content">
    <div class="intro-quote">简介：分享学习工具，各大专业通用</div>
    
    <div class="section-label">🆕 最新发布</div>
    <ul class="clean-list">
      {% for post in site.categories['奇技淫巧'] limit:3 %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
      {% else %}
        <li style="color:#ccc;">暂无文章</li>
      {% endfor %}
    </ul>

    {% if site.categories['奇技淫巧'].size > 3 %}
      <div class="section-label">🗄️ 历史归档</div>
      <ul class="clean-list">
        {% for post in site.categories['奇技淫巧'] offset:3 %}
          <li><a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
        {% endfor %}
      </ul>
    {% endif %}
  </div>
</details>


<details>
  <summary>
    <span class="category-title">3. 念两句诗</span>
    <span class="post-count">{{ site.categories['念两句诗'].size | default: 0 }}</span>
  </summary>
  <div class="expanded-content">
    <div class="intro-quote">简介：分享古文诗词，看得懂就看，看不懂反思下自己是不是中国人</div>
    
    <div class="section-label">🆕 最新发布</div>
    <ul class="clean-list">
      {% for post in site.categories['念两句诗'] limit:3 %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
      {% else %}
        <li style="color:#ccc;">暂无文章</li>
      {% endfor %}
    </ul>

    {% if site.categories['念两句诗'].size > 3 %}
      <div class="section-label">🗄️ 历史归档</div>
      <ul class="clean-list">
        {% for post in site.categories['念两句诗'] offset:3 %}
          <li><a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
        {% endfor %}
      </ul>
    {% endif %}
  </div>
</details>

---

### 口腹之欲篇

<details> <summary>
    <span class="category-title">4. 山水如画</span>
    <span class="post-count">{{ site.categories['山水如画'].size | default: 0 }}</span>
  </summary>
  <div class="expanded-content">
    <div class="intro-quote">简介：分享游记，起家篇目</div>
    
    <div class="section-label">🆕 最新发布</div>
    <ul class="clean-list">
      {% for post in site.categories['山水如画'] limit:3 %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
      {% else %}
        <li style="color:#ccc;">暂无文章</li>
      {% endfor %}
    </ul>

    {% if site.categories['山水如画'].size > 3 %}
      <div class="section-label">🗄️ 历史归档</div>
      <ul class="clean-list">
        {% for post in site.categories['山水如画'] offset:3 %}
          <li><a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
        {% endfor %}
      </ul>
    {% endif %}
  </div>
</details>


<details>
  <summary>
    <span class="category-title">5. 弄俩钱花</span>
    <span class="post-count">{{ site.categories['弄俩钱花'].size | default: 0 }}</span>
  </summary>
  <div class="expanded-content">
    <div class="intro-quote">简介：分享财经评论，不构成投资建议，市场有风险，投资需谨慎</div>
    
    <div class="section-label">🆕 最新发布</div>
    <ul class="clean-list">
      {% for post in site.categories['弄俩钱花'] limit:3 %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
      {% else %}
        <li style="color:#ccc;">暂无文章</li>
      {% endfor %}
    </ul>

    {% if site.categories['弄俩钱花'].size > 3 %}
      <div class="section-label">🗄️ 历史归档</div>
      <ul class="clean-list">
        {% for post in site.categories['弄俩钱花'] offset:3 %}
          <li><a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
        {% endfor %}
      </ul>
    {% endif %}
  </div>
</details>


<details>
  <summary>
    <span class="category-title">6. 打猫踹狗</span>
    <span class="post-count">{{ site.categories['打猫踹狗'].size | default: 0 }}</span>
  </summary>
  <div class="expanded-content">
    <div class="intro-quote">简介：分享博主阴暗的内心，付费高级用户可解锁</div>
    
    <div class="section-label">🆕 最新发布</div>
    <ul class="clean-list">
      {% for post in site.categories['打猫踹狗'] limit:3 %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
      {% else %}
        <li style="color:#ccc;">暂无文章</li>
      {% endfor %}
    </ul>

    {% if site.categories['打猫踹狗'].size > 3 %}
      <div class="section-label">🗄️ 历史归档</div>
      <ul class="clean-list">
        {% for post in site.categories['打猫踹狗'] offset:3 %}
          <li><a href="{{ post.url }}">{{ post.title }}</a> <span class="date-tag">{{ post.date | date: "%Y-%m-%d" }}</span></li>
        {% endfor %}
      </ul>
    {% endif %}
  </div>
</details>
