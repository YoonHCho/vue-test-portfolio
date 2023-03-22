<template>
  <div :class="[`bg-${theme}`, `${textColor}`, 'container', 'contact-container', 'mt-3', 'mb-3']">
    <form action="https://formsubmit.co/377129fb4873193394d35aadd3682a3b" method="POST" class="p-1 mt-1">
      <!-- HONEYPOT -->
      <input type="text" name="_honey" class="honey">

      <!-- Disable Captcha -->
      <input type="hidden" name="_captcha" value="false">

      <h1>Contact Me</h1>
      <label for="name" class="ps-2">Name</label>
      <input type="text" class="form-control mb-3" id="name" name="name" placeholder="Your Name">
      <label for="email" class="ps-2">Email</label>
      <input type="email" class="form-control mb-3" id="email" name="email" placeholder="Your Email Address" required>
      <label for="message" class="ps-2">Message</label>
      <textarea class="form-control mb-3" id="message" name="message" placeholder="Your Message" required></textarea>
      <div class="d-grid gap-2 d-md-flex justify-content-md-end">
        <button type="reset" class="btn btn-warning me-md-2">Reset</button>
        <button type="submit" class="btn btn-primary">Send</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  props: ['theme', 'textColor'],
  name: 'Contact'
}
</script>

<style scoped>
  .contact-container {
    width: 65%;
    border-radius: 10px;
  }
  .honey {
    display: none;
  }
  @media only screen and (max-width: 992px) {
    .contact-container {
      width: 90%;
    }
  }
  /* @media only screen and (min-width: 1200px) {
    .contact-container {
      width: 40%;
    }
  } */
</style>