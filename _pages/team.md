---
layout: page
title: 团队
permalink: /team/
description: 研究团队介绍
nav: true
---

<!-- 团队成员列表会自动从 _data/members.yml 渲染 -->

<div class="team">
{% for group in site.data.members %}
  <h2>{{ group.group }}</h2>
  <div class="row">
    {% for member in group.members %}
    <div class="col-sm-4">
      <div class="card">
        <img src="/assets/img/{{ member.photo }}" 
             alt="{{ member.name }}" class="card-img-top">
        <div class="card-body">
          <h5>{{ member.name }}</h5>
          <p>{{ member.role }}</p>
          {% if member.destination %}
            <p>📌 {{ member.destination }}</p>
          {% endif %}
          {% if member.research %}
            <p>🔬 {{ member.research }}</p>
          {% endif %}
          {% if member.email %}
            <p>✉️ {{ member.email }}</p>
          {% endif %}
        </div>
      </div>
    </div>
    {% endfor %}
  </div>
{% endfor %}
</div>
