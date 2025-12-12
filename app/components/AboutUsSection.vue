<template>
  <section class="px-4 lg:px-16 py-32 grid gap-16">
    <header>
      <SectionTitle>{{ $t('about.title') }}</SectionTitle>
      <SectionSubtitle>
        {{ $t('about.subtitle') }}
      </SectionSubtitle>
    </header>
    <div
      class="grid grid-cols-[auto_auto_1fr] gap-8 w-full max-w-4xl mx-auto relative"
    >
      <div
        class="hidden md:block absolute left-4.5 inset-y-24 w-1 bg-black animation-scrollspy"
      ></div>
      <AboutCard v-for="card in cards" :key="card.id" :card="card">
        <div class="absolute md:static -top-5 left-4">
          <div
            class="w-10 h-10 bg-black border-2 border-white grid place-items-center rounded-full text-lg text-white"
          >
            {{ card.id }}
          </div>
        </div>

        <div
          class="border-2 border-slate-900 rounded-2xl col-span-full md:col-span-2 grid md:grid-cols-subgrid items-center gap-4 p-4"
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
      </AboutCard>
    </div>
  </section>
</template>

<script setup lang="ts">
const cards = computed(() => {
  return [
    {
      id: 1,
      image: '/img/price.svg',
      title: $t('about.cards.c1.title'),
      description: $t('about.cards.c1.description'),
    },
    {
      id: 2,
      image: '/img/shelves.svg',
      title: $t('about.cards.c2.title'),
      description: $t('about.cards.c2.description'),
    },
    {
      id: 3,
      image: '/img/connections.svg',
      title: $t('about.cards.c3.title'),
      description: $t('about.cards.c3.description'),
    },
    {
      id: 4,
      image: '/img/orchestration.svg',
      title: $t('about.cards.c4.title'),
      description: $t('about.cards.c4.description'),
    },
  ]
})
</script>

<style lang="postcss" scoped>
.animation-scrollspy {
  scale: 1 0;
  transform-origin: top;
  animation: scrollspy linear forwards;
  animation-timeline: view(60vh 0px);
}

@keyframes scrollspy {
  to {
    scale: 1 1;
  }
}
</style>
