<template>
  <section class="bg-black relative sticky z-30 md:h-lvh px-4 py-10 md:p-20 text-white overflow-hidden">

    <div class="relative hidden md:flex h-full z-20 max-w-6xl mx-auto flex flex-col gap-6 md:gap-8 justify-center">

      <h2
        class="font-bricolage hidden md:block text-4xl lg:text-[350%] font-extrabold cursor-pointer transition-colors duration-500 aos-init aos-animate"
        data-aos="fade-right"
        :class="active === 'vision' ? 'text-white' : 'text-gray-800'"
        @mouseenter="active = 'vision'"
      >
        OUR <span>VISION</span>
      </h2>

      <h2
        class="font-bricolage hidden md:block text-4xl lg:text-[350%] font-bold cursor-pointer transition-colors duration-500 aos-init aos-animate"
        data-aos="fade-right"
        :class="active === 'mission' ? 'text-white' : 'text-gray-800'"
        @mouseenter="active = 'mission'"
      >
        OUR <span>MISSION</span>
      </h2>

    </div>

    <div class="absolute right-110 lg:right-150 top-1/6 bottom-4/6 -translate-y-1/2 hidden md:block">
      <div
        class="absolute h-[550px] w-[350px] lg:w-[450px] bg-[#202020] text-white flex flex-col justify-center gap-8 p-10 p-8 transition-all duration-700 ease-in-out shadow-[0_12px_28px_rgba(0,0,0,0.22)]"
        :class="active === 'vision'
          ? 'opacity-100 translate-x-0 rotate-[3.5deg] z-20'
          : 'opacity-0 translate-x-10 rotate-6 z-10'"
      >
        <h3 class="text-4xl font-semibold text-[#575757] mb-4">VISION</h3>
        <p class="text-2xl leading-relaxed">
          A world where African MSMEs are empowered to thrive because of easy-to-use
          and affordable digital business support solutions.
        </p>
        <ColorBar />
      </div>

      <div
        class="absolute h-[550px] w-[400px] lg:w-[450px] bg-[#202020] text-white flex flex-col justify-center gap-8 p-10 p-8 transition-all duration-700 ease-in-out"
        :class="active === 'mission'
          ? 'opacity-100 translate-x-0 rotate-[7deg] z-20'
          : 'opacity-0 translate-x-10 rotate-6 z-10'"
      >
        <h3 class="text-4xl font-semibold text-[#575757] mb-4">MISSION</h3>
        <p class="text-2xl leading-relaxed">
          To empower African MSMEs to scale sustainably by providing growth
          infrastructure, funding access, and strategic visibility through digital innovation.
        </p>
        <ColorBar />
      </div>

    </div>

    <div class="flex flex-col text-white gap-10 w-full justify-center items-center md:hidden py-10">
      <div class="bg-[#202020] flex flex-col items-start justify-center gap-8 px-4 py-10 aos-init aos-animate" data-aos="zoom-in-up">
        <h3 class="font-sans text-4xl leading-[110%] font-bold mb-3 uppercase ">
          <span class="text-[#575757] font-semibold">
              Our
          </span>Vision
        </h3>
        <p class="text-base leading-[150%]">
          A world where African MSMEs are empowered to thrive because of easy-to-use
          and affordable digital business support solutions.
        </p>
        <ColorBar />
      </div>

      <div class="bg-[#202020] flex flex-col items-start justify-center gap-9 px-4 py-10 aos-init aos-animate" data-aos="zoom-in-up">
        <h3 class="text-4xl leading-[110%] font-bold mb-3 uppercase ">
          <span class="text-[#575757] font-semibold">
              Our
          </span>Mission
        </h3>
        <p class="text-base leading-[150%]">
          To empower African MSMEs to scale sustainably by providing growth infrastructure,
          funding access, and strategic visibility through digital innovation.
        </p>
        <ColorBar />
      </div>

      <!-- <div class="bg-neutral-900 p-6 rounded-lg">
        <h3 class="text-lg font-semibold text-gray-400 mb-3">OUR MISSION</h3>
        <p class="text-sm">
          To empower African MSMEs to scale sustainably by providing growth infrastructure,
          funding access, and strategic visibility through digital innovation.
        </p>
      </div> -->
    </div>

  </section>
</template>

<script setup>
import { ref } from 'vue'
import ColorBar from './ColorBar.vue';

const active = ref('vision')
</script>
