<template>
  <section
    class="sticky z-30 px-4 md:p-20 py-10 bg-[#191919] flex flex-col items-start gap-10 md:gap-20 text-left"
  >
    <h3
      class="text-3xl font-extrabold md:text-5xl text-gray-600 font-bricolage uppercase max-w-[1100px] leading-[125%] md:leading-[110%]"
    >
      Why African Entrepreneurs Deserve Better Support
    </h3>

    <div class="grid grid-cols-3 md:gap-10">
      <div class="hidden md:block col-span-1">
        <img src="/assets/koppoh-in-koppoh.svg" alt="Koppoh in Koppoh" />
      </div>

      <div class="col-span-3 md:col-span-2 space-y-8">
        <p
          v-for="(item, index) in items"
          :key="index"
          ref="paragraphs"
          :class="[
            'text-2xl md:text-[32px] leading-[125%] transition-colors duration-700 ease-out',
            activeIndexes.includes(index) ? 'text-white' : 'text-[#575757]'
          ]"
        >
          {{ item }}
        </p>
      </div>
    </div>
  </section>
</template>



<script>
export default {
  data() {
    return {
      items: [
        "From the busy market stalls in Kano to the roadside workshops in Aba, the promising business in Yaba, and beyond Nigeria's borders to every corner of Africa, you are the engine that moves our continent forward.",
        "MSMEs like yours represent over 90% of businesses, contribute over 50% to GDP, and account for about 63% of employment in Africa. Yet 8 out of 10 businesses close before their fifth year.",
        "Not because you're not trying. But because you're building alone, with no structured business training, limited access to funding, nobody to help you manage growth, and no platform to tell your story.",
      ],
      activeIndexes: [],
    };
  },

  mounted() {
    const observer = new IntersectionObserver(
      entries => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            const index = this.$refs.paragraphs.indexOf(entry.target);
            if (!this.activeIndexes.includes(index)) {
              setTimeout(() => {
                this.activeIndexes.push(index);
              }, 150);
            }
          }
        });
      },
      {
        rootMargin: '-40% 0px -40% 0px',
        threshold: 0,
      }
    );

    this.$refs.paragraphs.forEach(p => observer.observe(p));
  },
};
</script>