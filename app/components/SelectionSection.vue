<template>
  <section class="px-4 lg:px-16 py-32 bg-slate-100 grid gap-16">
    <header>
      <SectionTitle>{{ $t('selection.title') }}</SectionTitle>
      <SectionSubtitle>
        {{ $t('selection.subtitle') }}
      </SectionSubtitle>
    </header>
    <div class="grid md:grid-cols-3 gap-8">
      <SelectionCard class="bg-brand-blue text-white">
        <template #icon>
          <SvgHand class="h-12" />
        </template>
        <template #title>{{ $t('selection.cards.blue.title') }}</template>
        {{ $t('selection.cards.blue.description') }}
      </SelectionCard>
      <SelectionCard class="bg-brand-orange text-black">
        <template #icon>
          <SvgVideo class="h-12" />
        </template>
        <template #title>{{ $t('selection.cards.orange.title') }}</template>
        {{ $t('selection.cards.orange.description') }}
      </SelectionCard>
      <SelectionCard class="bg-slate-200 text-black">
        <template #icon>
          <SvgPerson class="h-12" />
        </template>
        <template #title> {{ $t('selection.cards.gray.title') }} </template>
        {{ $t('selection.cards.gray.description') }}
      </SelectionCard>
    </div>
  </section>
</template>

<script setup lang="ts"></script>

<style lang="postcss" scoped></style>
