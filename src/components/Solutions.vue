<template>
    <section class="bg-white sticky z-30 flex flex-col items-start gap-10 md:gap-20 px-4 py-10 md:p-20">
        <div class="flex flex-col gap-4 md:gap-4">
            <h2 data-aos="fade-right" data-aos-offset="200"
                class="font-bricolage uppercase font-extrabold text-[40px] md:text-[64px] md:leading-[110%] max-w-[1100px] aos-init aos-animate">
                Our solutions for you
            </h2>
            <p data-aos="fade-right" data-aos-offset="200"
                class="md:text-xl aos-init aos-animate">
                With our digital solutions, you get everything you need in one place to succeed.
            </p>

        </div>
        <div v-for="(program, index) in programs" :key="index"
            class="flex flex-col md:flex-row justify-between gap-8 py-10 border-b border-gray-200">

            <div class="max-w-[8rem]">
                <h3 class="uppercase text-xl font-bold text-gray-700">
                    {{ program.title }}
                </h3>
                <ColorBar />
            </div>

            <div class="max-w-xl">
                <p class="text-sm leading-relaxed">
                {{ program.description }}
                </p>
            </div>

            <div>
                <button :class="[
                    'px-6 py-2 rounded-full text-sm font-medium transition',
                    program.buttonText === 'Find Out More'
                        ? 'bg-green-600 text-white hover:bg-green-700'
                        : 'bg-gray-200 text-gray-500 cursor-not-allowed'
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