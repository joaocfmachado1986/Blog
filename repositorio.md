---
layout: default
title: Publicações e Repositório
---

<div class="post-card">
    <h1 style="color: #0f4c5c; margin-bottom: 2rem;">Repositório Completo</h1>
    <p style="margin-bottom: 3rem; color: #64748b;">Abaixo você encontra a listagem integral de artigos, pesquisas e documentos técnicos publicados.</p>

    <div class="grid-publicacoes">
      {% for post in site.posts %}
        <div class="card-pub">
            <span class="card-date">{{ post.date | date: "%d %b %Y" }}</span>
            <a href="{{ post.url }}">{{ post.title }}</a>
            <div class="card-excerpt">
                {{ post.content | strip_html | truncatewords: 20 }}
            </div>
        </div>
      {% endfor %}
    </div>
</div>
