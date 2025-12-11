<template>
  <section class="px-4 lg:px-16 bg-slate-100 py-32">
    <div
      class="grid gap-16 lg:grid-cols-[auto_1fr] items-end w-full max-w-7xl mx-auto"
    >
      <h2 class="text-8xl lg:text-[120px] font-black text-black">FAQ</h2>
      <div class="grid gap-16">
        <p class="text-3xl font-semibold">
          {{ $t('faq.description') }}
        </p>
        <UAccordion
          :items="items"
          :ui="{
            trigger: 'text-3xl text-black',
            body: 'text-lg',
          }"
        />
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const items = ref([
  {
    label: $t('faq.items.q1.label'),
    content: $t('faq.items.q1.content'),
  },
  {
    label: $t('faq.items.q2.label'),
    content: $t('faq.items.q2.content'),
  },
  {
    label: $t('faq.items.q3.label'),
    content: $t('faq.items.q3.content'),
  },
  {
    label: $t('faq.items.q4.label'),
    content: $t('faq.items.q4.content'),
  },
])
</script>

<style lang="postcss" scoped></style>
