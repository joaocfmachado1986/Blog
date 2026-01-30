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

<section>
    <div class="grid-publicacoes">
      {% for post in site.posts limit:6 %}
        <div class="card-pub">
            <span class="card-date">{{ post.date | date: "%d %b %Y" }}</span>
            <a href="{{ post.url }}">{{ post.title }}</a>
            <div class="card-excerpt">
                {{ post.content | strip_html | truncatewords: 20 }}
            </div>
        </div>
      {% endfor %}
    </div>
</section>

<section class="grid-recursos">
    <a href="/arquivos/norma-fab.pdf" class="card-recurso" target="_blank">
        <strong>Normativa FAB</strong>
        <span style="font-size: 0.7rem; font-weight: bold;">📥 BAIXAR PDF</span>
    </a>
    <a href="/arquivos/norma-eb.pdf" class="card-recurso" target="_blank">
        <strong>Normativa EB</strong>
        <span style="font-size: 0.7rem; font-weight: bold;">📥 BAIXAR PDF</span>
    </a>
    <a href="/arquivos/norma-mb.pdf" class="card-recurso" target="_blank">
        <strong>Normativa MB</strong>
        <span style="font-size: 0.7rem; font-weight: bold;">📥 BAIXAR PDF</span>
    </a>
</section>

<section id="contacto">
    <div class="contact-box">
        <h3 style="margin: 0 0 1rem 0; font-weight: 800; color: #1e293b;">Contato</h3>
        <p style="margin-bottom: 2rem; font-size: 0.95rem; text-align: justify;">Convido o leitor ao contato para o envio de dúvidas, críticas, sugestões, diálogos acadêmicos, parcerias profissionais e trocas de experiências. Utilize o formulário abaixo e terei a satisfação de retornar em breve. Obrigado pelo interesse!</p>
        
        <form action="https://formspree.io/f/mbdypapq" method="POST" class="contact-form">
            <input type="text" name="name" placeholder="Seu Nome" required>
            <input type="email" name="_replyto" placeholder="Seu E-mail" required>
            <textarea name="message" rows="5" placeholder="Sua Mensagem" required></textarea>
            <button type="submit" class="btn-enviar">Enviar Mensagem</button>
        </form>
    </div>
</section>
