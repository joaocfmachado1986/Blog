---
layout: default
title: Home
---

<section style="display: flex; align-items: center; gap: 3rem; background: white; padding: 3rem; border-radius: 15px; border: 1px solid #e2e8f0;">
    <img src="/foto-perfil.jpg" style="width: 130px; height: 130px; border-radius: 50%; object-fit: cover; border: 4px solid #f1f5f9;" alt="João Machado">
    <div>
        <h1 style="margin: 0; font-size: 1.8rem; color: #0f4c5c; font-weight: 800;">Bem-vindo!</h1>
        <p style="margin: 1rem 0 0; color: #64748b; font-size: 1.05rem; text-align: justify; line-height: 1.7;">
            Aqui eu compartilho pesquisas e ideias de minha autoria ou de autores de meu interesse, além de documentos, sobretudo relacionados às minhas áreas de interesse, como Direito Aeronáutico, Base Industrial de Defesa, Políticas Públicas, Manutenção Aeronáutica e Normas Militares de Certificação de Empresas de Manutenção Aeronáutica. <a href="/sobre" style="color: #0f4c5c; font-weight: 700; text-decoration: underline;">Clique aqui</a> para saber mais sobre mim.
        </p>
    </div>
</section>

<section>
    <div class="grid-publicacoes">
      {% for post in site.posts limit:6 %}
        <div class="card-base card-pub">
            <span class="card-date">{{ post.date | date: "%d %b %Y" }}</span>
            <a href="{{ post.url }}">{{ post.title }}</a>
            <div class="card-excerpt">
                {{ post.content | strip_html | truncatewords: 25 }}
            </div>
        </div>
      {% endfor %}
    </div>
</section>

<section class="grid-recursos">
    <a href="/arquivos/norma-fab.pdf" class="card-base card-download" target="_blank">
        <strong>Normativa FAB: ICA 65-36</strong>
        <span>Baixar PDF</span>
    </a>
    <a href="/arquivos/norma-eb.pdf" class="card-base card-download" target="_blank">
        <strong>Normativa EB: EB30-N-40.105</strong>
        <span>Baixar PDF</span>
    </a>
    <a href="/arquivos/norma-mb.pdf" class="card-base card-download" target="_blank">
        <strong>Normativa MB: DGMM-3009</strong>
        <span>Baixar PDF</span>
    </a>
</section>

<section id="contacto">
    <div class="contact-box">
        <h2 style="margin: 0 0 1.5rem 0; font-weight: 800; color: #0f4c5c; font-size: 1.8rem;">Contato</h2>
        <p style="color: #475569; font-size: 1rem; text-align: justify;">
            Convido o leitor ao contato para o envio de dúvidas, críticas, sugestões, diálogos acadêmicos, parcerias profissionais e trocas de experiências. Utilize o formulário abaixo e terei a satisfação de retornar em breve. Obrigado pelo interesse!
        </p>
        
        <form action="https://formspree.io/f/mbdypapq" method="POST" class="contact-form">
            <input type="text" name="name" placeholder="Nome Completo" required>
            <input type="email" name="_replyto" placeholder="Seu e-mail" required>
            <textarea name="message" rows="6" placeholder="Como posso ajudar?" required></textarea>
            <button type="submit" class="btn-enviar">Enviar Mensagem</button>
        </form>
    </div>
</section>
