<script setup>
import { ref } from 'vue';
import Popup from '@/components/Popup/Popup.vue';

const isPopupActive = ref(false);
const isMenuActive = ref(false);
const currentForm = ref('signup');

const openModal = (form) => {
  currentForm.value = form;
  document.body.style.overflow = !isPopupActive.value ? 'hidden' : '';
  isPopupActive.value = true;
};

const closeModal = () => {
  document.body.style.overflow = !isPopupActive.value ? 'hidden' : '';
  isPopupActive.value = false;
};
const toggleMenu = () => {
  isMenuActive.value = !isMenuActive.value;
  document.body.style.overflow = isMenuActive.value ? 'hidden' : '';
};
</script>

<template>
  <header class="header">
    <div v-if="isMenuActive" class="header__overlay" @click="toggleMenu()"></div>
    <div class="header__wrapper">
      <div class="header__content">
        <div class="header__navigation">
          <a href="" class="header__logo">
            <img src="@/assets/images/logo.svg" alt="Logo" />
          </a>
          <nav :class="['header__menu', { active: isMenuActive }]">
            <button class="header__close-btn" @click="toggleMenu()">✕</button>
            <ul class="header__menu-items">
              <li class="header__menu-item">
                <a href="" data-text="Games">Games</a>
              </li>
              <li class="header__menu-item">
                <a href="" data-text="Contact Us">Contact Us</a>
              </li>
              <li class="header__menu-item">
                <a href="" data-text="Terms of Use">Terms of Use</a>
              </li>
              <li class="header__menu-item">
                <a href="" data-text="About">About</a>
              </li>
            </ul>
          </nav>
        </div>
        <div class="header__account">
          <button class="header__account-btn" @click="openModal('signup')" data-text="Sign up">
            Sign up
          </button>
          <button class="header__account-btn" @click="openModal('login')" data-text="Log in">
            Log in
          </button>
          <button class="header__burger-btn" @click="toggleMenu()">☰</button>
        </div>
      </div>
    </div>
    <Popup
      v-if="isPopupActive"
      :form="currentForm"
      @onUpdate:form="currentForm = $event"
      @close="closeModal"
    />
  </header>
</template>

<style lang="scss" scoped src="./Header.scss"></style>
