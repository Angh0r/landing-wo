<template>
  <NuxtLink
    :to="$localePath({ name: 'contact' })"
    class="bg-brand-orange text-white px-6 py-3 rounded-full hover:scale-95 transition-all duration-500"
  >
    {{ $t('become_a_tester') }}
  </NuxtLink>
</template>

<script setup lang="ts"></script>

<style lang="postcss" scoped></style>
