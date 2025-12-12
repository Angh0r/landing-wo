<template>
  <div class="grid grid-cols-subgrid col-span-full items-center relative">
    <div class="absolute md:static -top-5 left-4">
      <div
        class="w-10 h-10 bg-black border-2 border-white grid place-items-center rounded-full text-lg text-white"
      >
        {{ card.id }}
      </div>
    </div>

    <div
      class="border-2 border-slate-900 rounded-2xl col-span-full md:col-span-2 grid md:grid-cols-subgrid items-center gap-4 p-4 animation-reveal"
    >
      <img :src="card.image" class="h-64 mx-auto" alt="" />

      <div class="grid gap-4">
        <p
          class="text-2xl md:text-3xl font-semibold tracking-tighter text-black"
        >
          {{ card.title }}
        </p>
        <p>
          {{ card.description }}
        </p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  card: {
    id: number
    image: string
    title: string
    description: string
  }
}>()
</script>

<style lang="postcss" scoped>
.animation-reveal {
  opacity: 0;
  animation: reveal linear forwards;
  animation-timeline: view(60vh 0);
}

@keyframes reveal {
  to {
    opacity: 1;
  }
}
</style>
