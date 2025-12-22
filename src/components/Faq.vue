<template>
  <section class="sticky z-30 bg-gray-100 py-10 md:py-30">
    <div class="max-w-6xl px-4 md:px-20 flex flex-col gap-4 md:gap-10">

      <div>
        <h2 class="uppercase font-bricolage text-4xl md:text-6xl font-extrabold leading-tight">
          Frequently asked question
        </h2>
      </div>

      <div class="w-full grid grid-cols-12 gap-6">
        <div class="col-span-4">
            
        </div>
        <div class="col-span-12 md:col-span-8 flex flex-col">
            
        <div
          v-for="(faq, index) in faqs"
          :key="index"
          class="border-b border-gray-400 px-4 py-8"
        >
          
          <button
            @click="toggle(index)"
            class="w-full flex items-center justify-between text-left"
          >
            <h3 class="font-bricolage text-lg font-medium text-gray-900">
              {{ faq.question }}
            </h3>

            <p class="text-2xl font-light">
              {{ activeIndex === index ? '−' : '+' }}
            </p>
          </button>

          <transition
            enter-active-class="transition-all duration-300 ease-out"
            leave-active-class="transition-all duration-200 ease-in"
            enter-from-class="opacity-0 max-h-0"
            enter-to-class="opacity-100 max-h-40"
            leave-from-class="opacity-100 max-h-40"
            leave-to-class="opacity-0 max-h-0"
          >
            <p
              v-if="activeIndex === index"
              class="mt-4 text-sm text-gray-600 leading-relaxed max-w-xl"
            >
              {{ faq.answer }}
            </p>
          </transition>
        </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import { faqs } from '../utils';

const activeIndex = ref(0) 

const toggle = (index) => {
  activeIndex.value = activeIndex.value === index ? null : index
}
</script>