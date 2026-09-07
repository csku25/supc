+++
title = "Pedir Oración"
featured_image = "/img/banners/church.png"
+++

¿Necesitas oración? Siéntese libre de enviar una petición de oración. Incluye su nombre y la naturaleza de su necesidad. Su petición será enviada a nuestros guerreros de oración tan pronto que la recibimos.

<form id="prayer-form" class="prayer-request-form black-80 sans-serif mw6 center" accept-charset="UTF-8" action="https://formsubmit.co/spanishupc955@gmail.com" method="POST" role="form">

  <!-- Added id="email-subject" to make it targetable by JavaScript -->
  <input type="hidden" name="_subject" id="email-subject" value="Prayer Request" />
  <input type="hidden" name="_template" value="table" />
  <input type="hidden" name="_next" value="https://csku25.github.io/supc/prayer_request/thank_you/" />
  <input type="text" name="_honey" style="display:none" tabindex="-1" autocomplete="off" />

  <input type="text" id="name" name="Nombre" class="w-100 f5 pv3 ph3 bg-light-gray bn" required placeholder="Nombre Completo" aria-labelledby="name" />

  <textarea maxlength="300" id="request" name="Petición" class="w-100 f5 pv3 ph3 bg-light-gray bn" required placeholder="Escribe su petición aquí" aria-labelledby="request"></textarea>

  <input type="tel" id="phone" name="Número de Teléfono" class="w-100 f5 pv3 ph3 bg-light-gray bn" placeholder="Número de Teléfono (opcional)" aria-labelledby="phone" />

  <div class="tc mt4 mb3">
    <button type="submit" class="hero-button prayer-request-submit">Enviar</button>
  </div>

</form>

<!-- This script intercepts the submit button, pulls the user's name, and appends a dynamic timestamp -->
<script>
  document.getElementById('prayer-form').addEventListener('submit', function() {
    const subjectField = document.getElementById('email-subject');    
    const timeStamp = new Date().toLocaleTimeString(); 
    subjectField.value = "Prayer Request - " + timeStamp;
  });
</script>

