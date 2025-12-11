<template>
  <header
    class="bg-white shadow-sm sticky top-0 z-50 h-24 flex justify-between items-center px-4 lg:px-16"
  >
    <NuxtLink to="/">
      <SvgLogo class="h-10" />
    </NuxtLink>
    <div class="hidden lg:flex gap-8">
      <NuxtLink
        v-for="item in items"
        :key="item.label"
        :to="$localePath(item.to)"
        class="hover:text-brand-orange transition-colors"
      >
        {{ item.label }}
      </NuxtLink>
    </div>
    <div class="flex gap-4 items-center">
      <TesterButton class="hidden md:block" />
      <USlideover class="lg:hidden">
        <UButton icon="i-lucide-menu" color="neutral" variant="subtle" />

        <template #body>
          <div class="flex flex-col items-center gap-8">
            <TesterButton class="md:hidden" />
            <NuxtLink
              v-for="item in items"
              :key="item.label"
              :to="$localePath(item.to)"
              class="hover:text-brand-orange transition-colors"
            >
              {{ item.label }}
            </NuxtLink>
          </div>
        </template>
      </USlideover>
    </div>
  </header>
</template>

<script setup lang="ts">
const localePath = useLocalePath()

const items = computed(() => [
  {
    label: $t('main_menu.benefits'),
    to: localePath({ name: 'index', hash: '#benefits' }),
  },
  {
    label: $t('main_menu.how_it_works'),
    to: localePath({ name: 'index', hash: '#how-it-works' }),
  },
  {
    label: $t('main_menu.faq'),
    to: localePath({ name: 'index', hash: '#faq' }),
  },
])
</script>

<style lang="postcss" scoped></style>
