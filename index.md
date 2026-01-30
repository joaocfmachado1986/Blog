---
layout: default
title: Home
---

<div class="post-card" style="display: flex; align-items: center; gap: 2rem;">
    <img src="/foto-perfil.jpg" style="width: 100px; height: 100px; border-radius: 50%; object-fit: cover; border: 2px solid #e2e8f0;" alt="João Machado">
    <div>
        <h1 style="margin: 0; font-size: 1.8rem; color: #334155;">João Machado</h1>
        <p style="margin: 0.5rem 0 0; color: #64748b;">Especialista em Certificação e Pesquisa Científica Aeronáutica.</p>
    </div>
</div>

<div class="post-card">
    <h2 style="margin-top: 0; color: #0f4c5c;">Publicações</h2>
    <ul>
      {% for post in site.posts %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%d/%m/%Y" }}</li>
      {% endfor %}
    </ul>
</div>

<div class="post-card" id="contato">
    <h2 style="margin-top: 0; color: #0f4c5c;">Contato</h2>
    <p>Incentivo ao leitor a entrar em contato comigo caso tenham dúvidas, críticas ou sugestões. Preencha o formulário abaixo e em breve responderei. Obrigado!</p>

    <form action="https://formspree.io/f/mbdypapq" method="POST" class="contact-form">
        <input type="text" name="name" placeholder="Seu Nome" required style="width:100%; margin-bottom:10px; padding:8px;">
        <input type="email" name="email" placeholder="Seu E-mail" required style="width:100%; margin-bottom:10px; padding:8px;">
        <textarea name="message" placeholder="Sua Mensagem" required style="width:100%; margin-bottom:10px; padding:8px; height:100px;"></textarea>
        <button type="submit" class="btn-enviar">Enviar Mensagem</button>
    </form>
</div>
