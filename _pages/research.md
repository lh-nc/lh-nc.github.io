---
layout: page
title: 研究领域
permalink: /research/
display_categories: [活跃方向, 过往方向]  # 分类标签
horizontal: false   # 卡片排列方式（false=竖直，true=横向）
---

<!-- 每个研究方向 -->

<div class="projects">
  {% assign research_projects = site.projects | where: "category", "活跃方向" %}
  
  {% for project in research_projects %}
  <div class="card">
    <div class="card-body">
      <h3>{{ project.title }}</h3>
      <p>{{ project.description }}</p>
    </div>
  </div>
  {% endfor %}
</div>
