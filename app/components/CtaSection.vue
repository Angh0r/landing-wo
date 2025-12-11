<template>
  <section class="px-4 lg:px-16 py-32 flex flex-col items-center gap-8">
    <div
      class="flex flex-col items-center text-6xl font-black text-black uppercase tracking-tighter"
    >
      <p class="text-center">
        {{ $t('cta.title1') }}<br />
        {{ $t('cta.title2') }}
      </p>
      <p class="text-center">{{ $t('cta.title3') }}</p>
    </div>
    <p class="text-xl text-center">
      {{ $t('cta.description1') }}<br />
      {{ $t('cta.description2') }}
    </p>
    <TesterButton />
  </section>
</template>

<script setup lang="ts"></script>

<style lang="postcss" scoped></style>
