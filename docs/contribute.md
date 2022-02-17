---
layout: page
title: Contribute
permalink: /contribute/
---

If you want your phockheads featured on this website please [follow the instructions](https://github.com/mikeinspace/phockheads){:target="_blank"}.

If you don't know how to use git, you may submit your work via the form below. However, we can't promise your submissions will be processed in a reasonable using this method.

<form
  action="https://usebasin.com/f/1a1d2b97c41f"
  method="POST"
  enctype="multipart/form-data"
  id="my-contact-form"
>
<label for="email">Email <span class="small">(required)</span></label>
<input type="email" name="email" placeholder="john@doe.com" required />
<label for="message">Message <span class="small">(required)</span></label>
<textarea name="message" wrap="hard" required>
name: ASSET_NAME
author: ASSET_AUTHOR
image: https://i.imgur.com/ASSET_IMAGE.jpg
date: YYYY-MM-DD
description: A SHORT DESCRIPTION FOR THE SERIES
subs: 
  -
    name: FIRST_SUBASSET_NAME
    image: https://i.imgur/FIRST_SUBASSET_IMAGE.jpg
    supply: FIRST_SUBASSET_SUPPLY 
  -
    name: SECOND_SUBASSET_NAME
    image: https://i.imgur/SECOND_SUBASSET_IMAGE.jpg
    supply: SECOND_SUBASSET_SUPPLY 
</textarea>
<button type="submit" id="form-button">Send</button>
<div id="form-message"></div>
</form>

<script type="text/javascript">
var form = document.getElementById("my-contact-form");
var formMessage = document.getElementById("form-button");
var formButton = document.getElementById("form-button");
form.onsubmit = function(event) {
  event.preventDefault();
  formMessage.innerHTML = "Sending...";
  formMessage.disabled = true;
  var formData = new FormData(form);
  var xhr = new XMLHttpRequest();
  xhr.open("POST", form.action, true);
  xhr.onload = function(e) {
    console.log(xhr);
    if (xhr.status === 200) {
      formMessage.innerHTML = "Thank you!";
    } else {
      formMessage.innerHTML = "Please try again!"
      formMessage.disabled = false;
    }
  };
  xhr.send(formData);
};
</script>