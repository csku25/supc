+++
title = "Request Prayer"
featured_image = "/img/banners/church.png"
+++

Are you in need of prayer? Feel free to submit a prayer request by providing your name and the nature of your need. Your request will be forwarded to our prayer warriors as soon as we receive it.

<form id="prayer-form" class="prayer-request-form black-80 sans-serif mw6 center" accept-charset="UTF-8" action="https://formsubmit.co/spanishupc955@gmail.com" method="POST" role="form">

  <!-- Added id="email-subject" to make it targetable by JavaScript -->
  <input type="hidden" name="_subject" id="email-subject" value="Prayer Request" />
  <input type="hidden" name="_template" value="table" />
  <input type="hidden" name="_next" value="https://supcreading.com/prayer_request/thank_you/" />
  <input type="text" name="_honey" style="display:none" tabindex="-1" autocomplete="off" />

  <input type="text" id="name" name="Name" class="w-100 f5 pv3 ph3 bg-light-gray bn" required placeholder="Full Name" aria-labelledby="name" />

  <textarea maxlength="300" id="request" name="Request" class="w-100 f5 pv3 ph3 bg-light-gray bn" required placeholder="Enter your prayer request here" aria-labelledby="request"></textarea>

  <input type="tel" id="phone" name="Phone Number" class="w-100 f5 pv3 ph3 bg-light-gray bn" placeholder="Phone Number (optional)" aria-labelledby="phone" />

  <div class="tc mt4 mb3">
    <button type="submit" class="hero-button prayer-request-submit">Submit</button>
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

