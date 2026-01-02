---
layout: page
title: Blog
permalink: /blog/
---
<style>
  /* 每一个折叠大框的样式 */
  details {
    margin-bottom: 15px;
    border-bottom: 1px solid #eee; /* 只保留底部的分割线，更像目录 */
    padding-bottom: 10px;
  }

  /* 标题行（即开关）的样式 */
  summary {
    cursor: pointer;
    font-size: 1.2em; /* 字体加大，像个H3标题 */
    font-weight: bold;
    color: #333;
    padding: 10px 5px;
    outline: none;
    list-style: none; /* 隐藏默认的黑三角(部分浏览器) */
    display: flex; /* 让文字和篇数对齐 */
    justify-content: space-between; /* 篇数靠右显示，或者删掉这行让它紧跟标题 */
    align-items: center;
  }
  
  /* 针对Webkit内核隐藏默认三角 */
  summary::-webkit-details-marker {
    display: none;
  }

  /* 鼠标悬停时的效果 */
  summary:hover {
    color: #0366d6;
    background-color: #fcfcfc;
  }

  /* 篇数的样式 pill-badge */
  .post-count {
    font-size: 0.7em;
    font-weight: normal;
    color: #fff;
    background-color: #ddd;
    padding: 2px 8px;
    border-radius: 10px;
    margin-left: 10px;
  }
  /* 选中展开时，篇数变蓝 */
  details[open] .post-count {
    background-color: #0366d6;
  }

  /* 展开后的内容区域 */
  .expanded-content {
    margin-top: 10px;
    padding-left: 15px;
    animation: fadeIn 0.3s ease-in-out; /* 加个淡入动画 */
  }

  /* 简介块样式 */
  .intro-quote {
    color: #666;
    font-style: italic;
    font-size: 0.9em;
    border-left: 3px solid #ccc;
    padding-left: 10px;
    margin-bottom: 15px;
    background-color: #fafafa;
    padding: 8px;
  }

  /* 简单的淡入动画 */
  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(-5px); }
    to { opacity: 1; transform: translateY(0); }
  }
</style>

这是我的博客，点击栏目名称即可展开阅读。

---

### 鲲鹏之志篇

<details>
  <summary>
    <span>1. 指挥部署</span>
    <span class="post-count">{{ site.categories['指挥部署'].size | default: 0 }}</span>
  </summary>
  <div class="expanded-content">
    <div class="intro-quote">分享时事战略，一般很少更新，更多了号可能没了</div>
    <ul>
      {% for post in site.categories['指挥部署'] %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
      {% endfor %}
    </ul>
  </div>
</details>

<details>
  <summary>
    <span>2. 奇技淫巧</span>
    <span class="post-count">{{ site.categories['奇技淫巧'].size | default: 0 }}</span>
  </summary>
  <div class="expanded-content">
    <div class="intro-quote">分享学习工具，各大专业通用</div>
    <ul>
      {% for post in site.categories['奇技淫巧'] %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
      {% endfor %}
    </ul>
  </div>
</details>

<details>
  <summary>
    <span>3. 念两句诗</span>
    <span class="post-count">{{ site.categories['念两句诗'].size | default: 0 }}</span>
  </summary>
  <div class="expanded-content">
    <div class="intro-quote">分享古文诗词，看得懂就看，看不懂反思下自己是不是中国人</div>
    <ul>
      {% for post in site.categories['念两句诗'] %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
      {% endfor %}
    </ul>
  </div>
</details>

---

### 口腹之欲篇

<details open> <summary>
    <span>4. 山水如画</span>
    <span class="post-count">{{ site.categories['山水如画'].size | default: 0 }}</span>
  </summary>
  <div class="expanded-content">
    <div class="intro-quote">分享游记，起家篇目</div>
    <ul>
      {% for post in site.categories['山水如画'] %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
      {% endfor %}
    </ul>
  </div>
</details>

<details>
  <summary>
    <span>5. 弄俩钱花</span>
    <span class="post-count">{{ site.categories['弄俩钱花'].size | default: 0 }}</span>
  </summary>
  <div class="expanded-content">
    <div class="intro-quote">分享财经评论，不构成投资建议，市场有风险，投资需谨慎</div>
    <ul>
      {% for post in site.categories['弄俩钱花'] %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
      {% endfor %}
    </ul>
  </div>
</details>

<details>
  <summary>
    <span>6. 打猫踹狗</span>
    <span class="post-count">{{ site.categories['打猫踹狗'].size | default: 0 }}</span>
  </summary>
  <div class="expanded-content">
    <div class="intro-quote">分享博主阴暗的内心，付费高级用户可解锁</div>
    <ul>
      {% for post in site.categories['打猫踹狗'] %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <span style="font-size:0.8em; color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span></li>
      {% endfor %}
    </ul>
  </div>
</details>
