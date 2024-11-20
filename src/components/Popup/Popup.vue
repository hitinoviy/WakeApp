<script setup>
import { defineProps, defineEmits, ref, watch } from 'vue';
const password = ref('');
const confirmPassword = ref('');
const error = ref('');

const validatePasswords = () => {
  if (password.value !== confirmPassword.value) {
    error.value = 'Passwords dont match';
  } else {
    error.value = '';
  }
};
const props = defineProps({
  form: String,
});
const currentForm = ref(props.form);
const emit = defineEmits(['close']);

const changeForm = (nextForm) => {
  emit('onUpdate:form', nextForm);
};

const closePopup = () => {
  emit('close');
};
watch(
  () => props.form,
  (newVal) => {
    currentForm.value = newVal;
  }
);
</script>
<template>
  <div class="popup" @click.stop>
    <div class="overlay" @click="closePopup()"></div>
    <div class="popup__content">
      <div class="popup__header">
        <button
          class="popup__sign-btn"
          @click="changeForm('signup')"
          :class="{ active: currentForm === 'signup' }"
        >
          Sign Up
        </button>
        <button
          class="popup__login-btn"
          @click="changeForm('login')"
          :class="{ active: currentForm === 'login' }"
        >
          Login
        </button>
      </div>
      <form v-if="form === 'signup'" action="" class="popup__sign popup__form">
        <input type="text" placeholder="Firstname" name="firstname" class="popup__input" required />
        <input type="text" placeholder="Lastname" name="lastname" class="popup__input" required />
        <input type="email" placeholder="Email" name="email" class="popup__input" required />
        <div class="popup__password">
          <input
            v-model="password"
            type="password"
            placeholder="Password"
            name="password"
            class="popup__input"
            required
          />
          <input
            v-model="confirmPassword"
            type="password"
            placeholder="Confirm Password"
            required
            class="popup__input"
            @blur="validatePasswords"
          />
        </div>
        <p v-if="error" class="error-message">{{ error }}</p>
        <label class="popup__label">
          <input type="checkbox" name="" id="" />
          I accept the
          <a href="">Privacy Policy</a>
        </label>
        <button class="popup__submit-btn" type="submit">Join now</button>
      </form>
      <form v-else-if="form === 'login'" action="" class="popup__login popup__form">
        <input type="email" placeholder="Email" name="email" class="popup__input" required />
        <input
          v-model="password"
          type="password"
          placeholder="Password"
          name="password"
          class="popup__input"
          required
        />
        <button class="popup__submit-btn" type="submit">Login</button>
      </form>
    </div>
  </div>
</template>

<style lang="scss" scoped src="./Popup.scss"></style>
