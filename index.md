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
    <ul style="list-style: none; padding: 0;">
      {% for post in site.posts %}
        <li style="margin-bottom: 1rem; border-bottom: 1px solid #f1f5f9; padding-bottom: 10px;">
          <a href="{{ post.url }}" style="text-decoration: none; color: #334155; font-weight: 600;">{{ post.title }}</a>
          <span style="display: block; font-size: 0.8rem; color: #94a3b8;">{{ post.date | date: "%d/%m/%Y" }}</span>
        </li>
      {% endfor %}
    </ul>
    {% if site.posts.size == 0 %}
      <p style="color: #94a3b8; font-style: italic;">Nenhuma publicação disponível no momento.</p>
    {% endif %}
</div>

<div class="post-card" id="contato">
    <h2 style="margin-top: 0; color: #0f4c5c;">Contato</h2>
    <p style="font-size: 0.95rem;">Incentivo ao leitor a entrar em contato comigo caso tenham dúvidas, críticas ou sugestões. Estou igualmente à disposição para diálogos acadêmicos, parcerias profissionais e trocas de experiências. Utilize o formulário abaixo para entrar em contato comigo e terei a grata satisfação de retornar em breve. Obrigado pelo interesse!</p>

    <form action="https://formspree.io/f/mbdypapq" method="POST" class="contact-form">
        <input type="text" name="name" placeholder="Seu Nome" required>
        <input type="email" name="_replyto" placeholder="Seu E-mail" required>
        <textarea name="message" rows="4" placeholder="Sua Mensagem" required></textarea>
        <input type="text" name="_gotcha" style="display:none">
        <button type="submit" class="btn-enviar">Enviar Mensagem</button>
    </form>
</div>
