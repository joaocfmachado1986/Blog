---
layout: default
title: Home
---

<section style="display: flex; align-items: center; gap: 2.5rem; background: white; padding: 2.5rem; border-radius: 12px; border: 1px solid #e2e8f0;">
    <img src="/foto-perfil.jpg" style="width: 120px; height: 120px; border-radius: 50%; object-fit: cover; border: 3px solid #f1f5f9;" alt="João Machado">
    <div>
        <h1 style="margin: 0; font-size: 2rem; color: #1e293b;">Bem-vindo ao meu Portal</h1>
        <p style="margin: 0.5rem 0 0; color: #64748b; font-size: 1.1rem;">Explorações técnicas sobre <strong>Certificação Aeronáutica</strong>, Manutenção e Pesquisa Científica.</p>
    </div>
</section>

<section>
    <h2 class="section-title">Publicações Recentes</h2>
    <div class="grid-publicacoes">
      {% for post in site.posts %}
        <div class="card-pub">
            <a href="{{ post.url }}">{{ post.title }}</a>
            <span class="card-date">{{ post.date | date: "%d %b %Y" }}</span>
        </div>
      {% endfor %}
      {% if site.posts.size == 0 %}
        <p style="color: #94a3b8; font-style: italic;">As primeiras publicações estarão disponíveis em breve.</p>
      {% endif %}
    </div>
</section>

<section id="contacto">
    <h2 class="section-title">Contacto</h2>
    <div class="contact-box">
        <p style="margin-bottom: 2rem;">Incentivo ao leitor a entrar em contacto comigo caso tenham dúvidas, críticas ou sugestões. Estou igualmente à disposição para diálogos acadêmicos e parcerias profissionais.</p>
        
        <form action="https://formspree.io/f/mbdypapq" method="POST" class="contact-form">
            <input type="text" name="name" placeholder="Seu Nome" required>
            <input type="email" name="_replyto" placeholder="Seu E-mail" required>
            <textarea name="message" rows="5" placeholder="Sua Mensagem" required></textarea>
            <button type="submit" class="btn-enviar">Enviar Mensagem</button>
        </form>
    </div>
</section>
