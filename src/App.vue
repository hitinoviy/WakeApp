<script setup>
import Wrapper from '@/components/Wrapper/Wrapper.vue';
import Preloader from '@/components/Preloader/Preloader.vue';
import HeroBlock from '@/components/HeroBlock/HeroBlock.vue';
import GamesBlock from './components/GamesBlock/GamesBlock.vue';
import ContactBlock from './components/ContactBlock/ContactBlock.vue';
import { ref, onMounted } from 'vue';
//const loading = ref(true);

//onMounted(() => {
//  setTimeout(() => {
//    loading.value = false;
//  }, 2000);
//});
</script>

<template>
  <Preloader v-if="loading" />
  <Wrapper v-else>
    <HeroBlock />
    <GamesBlock />
    <ContactBlock />
  </Wrapper>
</template>

<style lang="scss">
@use '@/assets/main.scss';
</style>
