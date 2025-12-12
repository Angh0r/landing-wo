<template>
  <section class="px-4 lg:px-16 py-32 flex flex-col items-center gap-8">
    <div
      class="flex flex-col items-center text-4xl md:text-6xl font-black text-black uppercase tracking-tighter"
    >
      <p class="text-center animation-slide slide-right">
        {{ $t('cta.title1') }}<br />
        {{ $t('cta.title2') }}
      </p>
      <p class="text-center animation-slide slide-left">
        {{ $t('cta.title3') }}
      </p>
    </div>
    <p class="text-xl text-center">
      {{ $t('cta.description1') }}<br />
      {{ $t('cta.description2') }}
    </p>
    <TesterButton />
  </section>
</template>

<script setup lang="ts"></script>

<style lang="postcss" scoped>
@media (prefers-reduced-motion: no-preference) {
  .slide-right {
    animation: slide-right 0.5s ease-in-out;
    animation-timeline: view(40vh 0);
  }

  .slide-left {
    animation: slide-left 0.5s ease-in-out;
    animation-timeline: view(40vh 0);
  }
}

@keyframes slide-right {
  from {
    transform: translateX(-30%);
  }
  to {
    transform: translateX(0);
  }
}

@keyframes slide-left {
  from {
    transform: translateX(30%);
  }
  to {
    transform: translateX(0);
  }
}
</style>
