<template>
  <UButton
    size="xl"
    class="bg-brand-orange hover:bg-brand-orange text-white px-6 py-3 rounded-full hover:scale-95 transition-all duration-500"
    :to="$localePath({ name: 'contact' })"
  >
    {{ $t('become_a_tester') }}
  </UButton>
</template>

<script setup lang="ts"></script>

<style lang="postcss" scoped></style>
