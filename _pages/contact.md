---
layout: page
title: CONTACT
permalink: /contact/
nav: true
nav_order: 6
social: true
---
    
<!-- _pages/contact.md -->
<div style="text-align: center;">
  <p>Feel free to reach out to me using the form below:</p>
</div>

<!-- Contact Form -->
<div style="text-align: center; max-width: 500px; margin: 0 auto;">
  <form id="contactForm" method="post" enctype="text/plain" style="width: 100%; text-align: left;">
    <div style="margin-bottom: 20px;">
      <label for="name" style="display: block; margin-bottom: 8px; font-weight: bold;">Name:</label>
      <input type="text" id="name" name="name" style="width: 100%; padding: 10px; border-radius: 5px; border: 1px solid #ccc;" required>
    </div>

    <div style="margin-bottom: 20px;">
      <label for="email" style="display: block; margin-bottom: 8px; font-weight: bold;">Email:</label>
      <input type="email" id="email" name="email" style="width: 100%; padding: 10px; border-radius: 5px; border: 1px solid #ccc;" required>
    </div>

    <div style="margin-bottom: 20px;">
      <label for="message" style="display: block; margin-bottom: 8px; font-weight: bold;">Message:</label>
      <textarea id="message" name="message" rows="4" style="width: 100%; padding: 10px; border-radius: 5px; border: 1px solid #ccc;" required></textarea>
    </div>

    <input type="button" value="Submit" onclick="submitForm()" style="padding: 10px 20px; font-size: 16px; background-color: #007bff; color: #fff; border: none; border-radius: 5px; cursor: pointer;">
  </form>
</div>

<script>
function submitForm() {
  var message = document.getElementById("message").value;
  var mailtoLink = "mailto:cyprien.fol@usys.ethz.ch?body=" + encodeURIComponent(message);
  window.location.href = mailtoLink;
}
</script>

<!-- Social -->
{%- if page.social %}
<div style="text-align: center; margin-top: 100px;"> <!-- Added margin-top here -->
    <div class="social" style="margin-top: 10px;"> <!-- Added margin-top here -->
        <div class="contact-icons">
            {% include social.html %}
        </div>
    </div>
</div>


{%- endif %}