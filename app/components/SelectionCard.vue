<template>
  <div
    class="grid grid-rows-subgrid row-span-3 rounded-2xl overflow-hidden p-6 animation-reveal"
  >
    <div>
      <slot name="icon" />
    </div>
    <p class="text-3xl font-semibold">
      <slot name="title" />
    </p>
    <p>
      <slot />
    </p>
  </div>
</template>

<script setup lang="ts"></script>

<style lang="postcss" scoped></style>
