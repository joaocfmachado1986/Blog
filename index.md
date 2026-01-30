---
layout: default
title: Home
---

<div class="intro-card">
    <img src="/foto-perfil.jpg" class="profile-pic" alt="João Machado">
    <div>
        <h2 style="margin:0; color: #1e293b;">João Machado</h2>
        <p style="margin:5px 0 0; color:#64748b; font-size: 1.1rem;">Especialista em Certificação e Pesquisa Científica Aeronáutica.</p>
    </div>
</div>

<div class="post-card">
    <h3 style="margin-top: 0; color: #1e293b; border-bottom: 2px solid #eff6ff; padding-bottom: 10px;">
        Publicações e Insights Recentes
    </h3>
    
    <p style="color: #64748b; font-size: 0.9rem; margin-bottom: 1.5rem;">
        Explore as últimas análises técnicas e documentos de pesquisa científica disponibilizados abaixo.
    </p>

    <ul style="list-style: none; padding: 0;">
      {% for post in site.posts %}
        <li style="margin-bottom: 15px; padding: 10px; border-radius: 8px; background: #f8fafc; transition: transform 0.2s;">
          <a href="{{ post.url }}" style="text-decoration: none; color: #2563eb; font-weight: 600; font-size: 1.1rem;">
            {{ post.title }}
          </a>
          <div style="font-size: 0.8rem; color: #94a3b8; margin-top: 4px;">
            Publicado em {{ post.date | date: "%d/%m/%Y" }}
          </div>
        </li>
      {% endfor %}
    </ul>

    {% if site.posts.size == 0 %}
      <p style="color: #94a3b8; font-style: italic;">Nenhuma publicação encontrada no momento.</p>
    {% endif %}
</div>
