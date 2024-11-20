<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  imageUrl: {
    type: String,
    required: true,
  },
  title: {
    type: String,
    required: true,
  },
  text: {
    type: String,
    required: true,
  },
});
</script>
<template>
  <div class="games__card">
    <a href="">
      <img :src="imageUrl" alt="Game Image" />
      <div class="games__text">
        <h3>{{ title }}</h3>
        <p>{{ text }}</p>
      </div>
    </a>
  </div>
</template>
<style lang="css" scoped src="./GameBlock.scss"></style>
