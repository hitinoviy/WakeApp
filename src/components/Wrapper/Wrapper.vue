<script setup>
import Header from '@/components/Header/Header.vue';
import Footer from '@/components/Footer/Footer.vue';
</script>

<template>
  <div>
    <Header />
    <main class="wrapper__container">
      <slot></slot>
    </main>
    <Footer />
  </div>
</template>
