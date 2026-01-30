---
layout: default
title: Home
---

<section style="display: flex; align-items: center; gap: 2.5rem; background: white; padding: 2.5rem; border-radius: 12px; border: 1px solid #e2e8f0;">
    <img src="/foto-perfil.jpg" style="width: 120px; height: 120px; border-radius: 50%; object-fit: cover; border: 3px solid #f1f5f9;" alt="João Machado">
    <div>
        <h1 style="margin: 0; font-size: 2rem; color: #1e293b;">Bem-vindo!</h1>
        <p style="margin: 0.5rem 0 0; color: #64748b; font-size: 1rem; text-align: justify;">
            Aqui eu compartilho pesquisas e ideias de minha autoria ou de autores de meu interesse, além de documentos, sobretudo relacionado às minhas áreas de interesse, como Direito Aeronáutico, Base Industrial de Defesa, Políticas Públicas, Manutenção Aeronáutica e Normas Militares de Certificação de Empresas de Manutenção Aeronáutica. <a href="/sobre" style="color: #0f4c5c; font-weight: 600; text-decoration: underline;">Clique aqui</a> para saber mais sobre mim.
        </p>
    </div>
</section>

<section style="margin-top: 3rem;">
    <div class="grid-publicacoes">
      {% for post in site.posts %}
        <div class="card-pub">
            <a href="{{ post.url }}">{{ post.title }}</a>
            <span class="card-date">{{ post.date | date: "%d %b %Y" }}</span>
        </div>
      {% endfor %}
    </div>
</section>

<section id="contacto" style="margin-top: 3rem;">
    <div class="contact-box">
        <p style="margin-bottom: 2rem; font-size: 0.95rem;">Incentivo ao leitor a entrar em contato comigo caso tenham dúvidas, críticas ou sugestões. Estou igualmente à disposição para diálogos acadêmicos, parcerias profissionais e trocas de experiências. Utilize o formulário abaixo para entrar em contato comigo e terei a grata satisfação de retornar em breve. Obrigado pelo interesse!</p>
        
        <form action="https://formspree.io/f/mbdypapq" method="POST" class="contact-form">
            <input type="text" name="name" placeholder="Seu Nome" required>
            <input type="email" name="_replyto" placeholder="Seu E-mail" required>
            <textarea name="message" rows="5" placeholder="Sua Mensagem" required></textarea>
            <button type="submit" class="btn-enviar">Enviar Mensagem</button>
        </form>
    </div>
</section>
