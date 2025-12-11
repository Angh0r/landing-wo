<template>
  <footer class="bg-white py-24 grid gap-16 px-4 lg:px-16">
    <div class="flex flex-col lg:flex-row gap-8 justify-between items-center">
      <p class="text-black text-4xl font-semibold tracking-tighter">
        {{ $t('footer.simple_clear_on_demand') }}
      </p>
      <NuxtLink
        :to="$localePath({ name: 'contact' })"
        class="bg-brand-orange text-white px-6 py-3 rounded-full"
      >
        {{ $t('become_a_tester') }}
      </NuxtLink>
    </div>
    <div class="grid gap-8 md:grid-cols-2 text-lg font-semibold">
      <div class="grid gap-3">
        <p class="text-black">{{ $t('footer.about') }}</p>
        <NuxtLink
          :to="$localePath({ name: 'index', hash: '#how-it-works' })"
          class="text-slate-500 hover:text-slate-700 transition-colors"
        >
          {{ $t('footer.how_it_works') }}
        </NuxtLink>
        <NuxtLink
          :to="$localePath({ name: 'index', hash: '#perks' })"
          class="text-slate-500 hover:text-slate-700 transition-colors"
        >
          {{ $t('footer.perks') }}
        </NuxtLink>
      </div>
      <div class="grid gap-3">
        <p class="text-black">{{ $t('footer.policy') }}</p>
        <NuxtLink
          :to="$localePath({ name: 'rules' })"
          class="text-slate-500 hover:text-slate-700 transition-colors"
        >
          {{ $t('footer.rules') }}
        </NuxtLink>
        <NuxtLink
          :to="$localePath({ name: 'index', hash: '#faq' })"
          class="text-slate-500 hover:text-slate-700 transition-colors"
        >
          {{ $t('footer.faq') }}
        </NuxtLink>
      </div>
    </div>
    <div class="flex flex-col items-center gap-8">
      <SvgLogo class="h-20" />
      <p class="text-sm">
        {{ $t('footer.copyright', { year: new Date().getFullYear() }) }}
      </p>
    </div>
  </footer>
</template>

<script setup lang="ts"></script>

<style lang="postcss" scoped></style>
