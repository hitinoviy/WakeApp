<script setup></script>

<template>
  <div class="contact">
    <div class="contact__info">
      <div class="contact__title">
        <h2>Contact us</h2>
        <p>If you have some questions, send us a message</p>
      </div>
      <form action="" class="form">
        <div class="form__inputs">
          <input type="text" placeholder="Firstname" required />
          <input type="email" placeholder="Email Address" required />
          <textarea placeholder="Your message here..."></textarea>
        </div>
        <div class="form__policy">
          <div class="form__wrapper">
            <input type="checkbox" name="" id="form__policy2" />
            <label for="form__policy2">I Accept The <a href="#">Privacy Policy</a></label>
          </div>
          <button class="form__button" type="submit">Send</button>
        </div>
      </form>
    </div>
    <div class="contact__image">
      <img src="@/assets/images/image.png" alt="" />
    </div>
  </div>
</template>

<style lang="scss" scoped src="./ContactBlock.scss"></style>
