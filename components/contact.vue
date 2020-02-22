<template>
  <div class="container">
    <h1 class="title">Contact</h1>
    <div class="content">
      <form name="contact" action method="post" netlify>
        <label class="form-label" for="name">Name:</label>
        <input type="hidden" name="form-name" value="contact" />
        <input class="form-field" name="name" id="name" />
        <label class="form-label" for="email">Email:</label>
        <!-- <input type="hidden" name="form-email" value="contact" /> -->
        <input class="form-field" name="email" id="email" />
        <label class="form-label" for="message">Message:</label>
        <!-- <input type="hidden" name="form-message" value="contact" /> -->
        <textarea class="form-field" name="message" id="message"></textarea>
        <input class="form-button" type="submit" value="Send message" />
      </form>
    </div>
  </div>
</template>