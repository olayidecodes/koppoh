<template>
  <div class="sticky">
    <Header />
    <Hero />
    <Intro />
    <Solutions />
  </div>
</template>

<script setup>
import { onMounted } from 'vue';
import Header from './components/Header.vue';
import Hero from './components/Hero.vue';
import Intro from './components/Intro.vue';
import Solutions from './components/Solutions.vue';
import AOS from 'aos';
import 'aos/dist/aos.css'
onMounted(() => {
  AOS.init();
})
</script>
