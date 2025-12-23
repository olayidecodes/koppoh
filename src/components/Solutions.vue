<template>
    <section class="bg-white sticky z-30 flex flex-col items-start gap-10 md:gap-20 px-4 py-10 md:p-20">
        <div class="flex flex-col gap-4 md:gap-4">
            <h2 data-aos="fade-right" data-aos-offset="200"
                class="font-bricolage uppercase font-extrabold text-[40px] md:text-[64px] md:leading-[110%] max-w-[1100px] aos-init aos-animate">
                Our solutions for you
            </h2>
            <p data-aos="fade-right" data-aos-offset="200"
                class="md:text-xl aos-init aos-animate max-w-140">
                With our digital solutions, you get everything you need in one place to succeed.
            </p>

        </div>
        <div v-for="(program, index) in programs" :key="index"
            class="w-full flex flex-col md:flex-row justify-between md:items-center gap-8 md:py-10 lg:px-20 pb-13 md:pb-30 md:border-b border-gray-200 aos-init aos-animate"
            data-aos="zoom-in-up"
            :data-aos-delay="program.delay"
  :data-aos-offset="program.offset"
            >
            <div class="md:max-w-[12rem]">
                <h3 class="uppercase text-2xl font-bold text-gray-800 pb-4">
                    {{ program.title }}
                </h3>
                <ColorBar />
            </div>

            <div class="md:max-w-xl">
                <p class="text-sm font-medium leading-6">
                {{ program.description }}
                </p>
            </div>

            <div>
                <button :class="[
                    'py-3 w-35 rounded-full text-sm transition',
                    program.buttonText === 'Find Out More'
                        ? 'bg-green-600 text-white hover:bg-green-700'
                        : 'bg-gray-200 text-white cursor-not-allowed'
                ]">
                    {{ program.buttonText }}
                </button>
            </div>
        </div>
    </section>
</template>
<script setup>
import { programs } from '../utils';
import ColorBar from './ColorBar.vue';

</script>