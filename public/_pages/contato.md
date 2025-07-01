---
layout: default
title: Contato
subtitle: 
permalink: /contato
header_type: "hero"
show_breadcrumb  : true
breadcrumb_list :
  - label: Home
    url: /
  - label: Contato
    url: /contato/
---

Entre em contato conosco através do formulário abaixo ou envie um e-mail para <a href="mailto:{ site.email }}"> {{ site.email }} </a>.

<div class="row">
  <div class="col-md-6">
    <form id="contact-form" method="post" action="/contato/">
      <div class="form-group">
        <label for="name">Nome</label>
        <input type="text" class="form-control" id="name" name="name" required>
      </div>
      <div class="form-group">
        <label for="email">E-mail</label>
        <input type="email" class="form-control" id="email" name="email" required>
        </div>
        <div class="form-group">
        <label for="message">Mensagem</label>
        <textarea class="form-control" id="message" name="message" rows="5" required></textarea>
        </div>
        <button type="submit" class="btn btn-primary">Enviar</button>
    </form>
  </div>
    <div class="col-md-6">
        <h3>Informações de Contato</h3>
        <p><strong>E-mail:</strong> <a href="mailto:{{ site.email }}">{{ site.email }}</a></p>
        <p><strong>Telefone:</strong> {{ site.phone }}</p>
        <p><strong>Endereço:</strong> {{ site.address }}</p>
        <p><strong>Horário de Atendimento:</strong> {{ site.hours }}</p>
        <h3>Redes Sociais</h3>
        <ul class="list-unstyled">
            {% for social in site.social %}
                <li>
                    <a href="{{ social.url }}" target="_blank">
                        <i class="{{ social.icon }}"></i> {{ social.name }}
                    </a>
                </li>
            {% endfor %}
        </ul>
    </div>
</div>
<script>
document.getElementById('contact-form').addEventListener('submit', function(event) {
    event.preventDefault();
    
    // Aqui você pode adicionar a lógica para enviar o formulário, como uma requisição AJAX
    alert('Formulário enviado com sucesso!');
    
    // Limpar o formulário após o envio
    this.reset();
}); 
</script>

