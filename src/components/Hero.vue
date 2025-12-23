<template>
  <section
    class="sticky inset-0 z-10 bg-white flex flex-col items-start justify-stretch text-left pt-22 md:pt-24 p-4 md:p-20 min-h-svh"
  >
    <div class="flex flex-col items-start gap-10 max-w-[926px] mb-auto">
      <h1
        class="relative text-[40px] md:text-6xl lg:text-8xl font-bricolage font-extrabold text-black leading-[110%] uppercase opacity-0 translate-x-[-50px] animate-fade-slide-right"
        style="animation-delay: 0.2s;"
      >
        Driving prosperity for African businesses
      </h1>
      <div class="flex items-center gap-0 translate-x-[-40px] ">
        <div
          class="w-[46.67px] h-1 bg-[#2A2F9A] opacity-0 animate-fade-slide-right"
          style="animation-delay: 0.4s;"
        ></div>
        <div
          class="w-[46.67px] h-1 bg-[#D9961E] animate-fade-slide-right"
          style="animation-delay: 0.3s;"
        ></div>
        <div
          class="w-[46.67px] h-1 bg-[#0D8B1A] animate-fade-slide-right"
          style="animation-delay: 0.2s;"
        ></div>
      </div>
    </div>
    
      <div class="md:max-w-[536px]">
        <p
          class="text-base md:text-[22px] leading-[150%] md:leading-[125%] opacity-0 translate-x-[-50px] animate-fade-slide-right"
          style="animation-delay: 0.4s;"
        >
          Get the training, funding, visibility, and partners you need to build
          a Multi-Million Dollar Business.
        </p>
      </div>
  </section>
</template>
<script>

</script>

<style>
@keyframes fade-slide-right {
  0% {
    opacity: 0;
    transform: translateX(-50px);
  }
  100% {
    opacity: 1;
    transform: translateX(50px);
  }
}

.animate-fade-slide-right {
  animation: fade-slide-right 0.8s forwards;
}
</style>