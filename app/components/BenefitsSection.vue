<template>
  <section id="benefits" class="px-4 lg:px-16 py-32 grid gap-16 bg-slate-100">
    <header>
      <SectionTitle>{{ $t('benefits.title') }}</SectionTitle>
      <SectionSubtitle>{{ $t('benefits.subtitle') }}</SectionSubtitle>
    </header>
    <div
      class="grid md:grid-cols-2 lg:grid-cols-4 gap-4 w-full max-w-7xl mx-auto"
    >
      <div>
        <div class="bg-brand-blue rounded-2xl p-6 overflow-hidden text-white">
          <p class="text-2xl xl:text-3xl font-semibold pb-12 h-full lg:h-auto">
            {{ $t('benefits.cards.blue.title') }}
          </p>
          <p>
            {{ $t('benefits.cards.blue.description') }}
          </p>
        </div>
      </div>
      <div>
        <div
          class="bg-brand-orange rounded-2xl p-6 overflow-hidden text-black lg:mt-12 h-full lg:h-auto"
        >
          <p class="text-2xl xl:text-3xl font-semibold pb-12">
            {{ $t('benefits.cards.orange.title') }}
          </p>
          <p>
            {{ $t('benefits.cards.orange.description') }}
          </p>
        </div>
      </div>
      <div>
        <div
          class="bg-white rounded-2xl p-6 overflow-hidden text-black lg:mt-24 h-full lg:h-auto"
        >
          <p class="text-2xl xl:text-3xl font-semibold pb-12">
            {{ $t('benefits.cards.white.title') }}
          </p>
          <p>
            {{ $t('benefits.cards.white.description') }}
          </p>
        </div>
      </div>
      <div>
        <div
          class="bg-zinc-800 rounded-2xl p-6 overflow-hidden text-white lg:mt-36 h-full lg:h-auto"
        >
          <p class="text-2xl xl:text-3xl font-semibold pb-12">
            {{ $t('benefits.cards.dark.title') }}
          </p>
          <p>
            {{ $t('benefits.cards.dark.description') }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts"></script>

<style lang="postcss" scoped></style>
