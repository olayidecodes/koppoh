<template>
  <div class="sticky">
    <Header />
    <Hero />
    <Intro />
    <Vission />
    <Solutions />
    <Faq />
    <Footer />
  </div>
</template>

<script setup>
import { onMounted } from 'vue';
import AOS from 'aos';
import 'aos/dist/aos.css'
import Header from './components/Header.vue';
import Hero from './components/Hero.vue';
import Intro from './components/Intro.vue';
import Solutions from './components/Solutions.vue';
import Faq from './components/Faq.vue';
import Footer from './components/Footer.vue';
import Vission from './components/Vision.vue';
onMounted(() => {
  AOS.init();
})
</script>
