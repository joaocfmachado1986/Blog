---
layout: default
title: Home
---

<div class="intro-card">
<img src="/foto-perfil.jpg" class="profile-pic" alt="João Machado">
    <div class="intro-text">
        <h1>João Machado</h1>
        <p>Especialista em Certificação e Normatização Militar. Aqui compartilho pesquisas, documentos e análises sobre o setor aeronáutico e de manutenção de defesa.</p>
    </div>
</div>

## Últimas Publicações

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%d/%m/%Y" }}
    </li>
  {% endfor %}
</ul>
