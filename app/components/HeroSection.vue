<template>
  <section
    id="hero"
    class="px-4 lg:px-8 py-8 grid gap-16 min-h-[calc(100vh-96px)] overflow-hidden"
  >
    <UContainer class="relative grid place-items-center">
      <div class="flex flex-col lg:flex-row items-center lg:h-full gap-12">
        <div class="lg:w-3/5 grid gap-16">
          <div class="grid gap-8">
            <div
              class="text-black uppercase font-black text-2xl md:text-[clamp(2.5rem,calc(1rem+6vw),5rem)] lg:text-[clamp(4rem,calc(1rem+5vw),5rem)] leading-none flex flex-col items-center lg:items-start"
            >
              <p>{{ $t('hero.title.line1') }}</p>
              <p>{{ $t('hero.title.line2') }}</p>
              <p>{{ $t('hero.title.line3') }}</p>
            </div>
            <p class="text-2xl text-zinc-600">
              {{ $t('hero.subtitle') }}
            </p>
          </div>
          <div class="flex justify-center lg:justify-start">
            <TesterButton />
          </div>
        </div>

        <NuxtImg
          src="/img/mockup_macbook_magazyny.png"
          class="lg:object-cover h-auto lg:h-[70vh] w-full lg:overflow-visible lg:object-left"
        />
      </div>

      <div
        class="hidden lg:flex absolute bottom-0 w-full justify-center animate-[bounce_3s_ease-in-out_infinite]"
      >
        <p class="text-5xl text-zinc-300 rotate-90">&raquo;</p>
      </div>
    </UContainer>
  </section>
</template>

<script setup lang="ts"></script>

<style lang="postcss" scoped></style>
