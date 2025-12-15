<template>
  <section class="px-4 lg:px-16 py-32 bg-slate-100 lg:h-[3000px] relative">
    <div class="flex flex-col gap-16 sticky top-32">
      <header>
        <SectionTitle>{{ $t('benefits.title') }}</SectionTitle>
        <SectionSubtitle>{{ $t('benefits.subtitle') }}</SectionSubtitle>
      </header>
      <div
        class="grid md:grid-cols-2 lg:grid-cols-4 gap-4 w-full max-w-7xl mx-auto"
      >
        <div>
          <div
            class="bg-brand-blue rounded-2xl p-6 overflow-hidden text-white animation-reveal animation-show animation-show__blue"
          >
            <p
              class="text-2xl xl:text-3xl font-semibold pb-12 h-full lg:h-auto"
            >
              {{ $t('benefits.cards.blue.title') }}
            </p>
            <p>
              {{ $t('benefits.cards.blue.description') }}
            </p>
          </div>
        </div>
        <div>
          <div
            class="bg-brand-orange rounded-2xl p-6 overflow-hidden text-black lg:mt-12 h-full lg:h-auto animation-show animation-show__orange"
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
            class="bg-white rounded-2xl p-6 overflow-hidden text-black lg:mt-24 h-full lg:h-auto animation-show animation-show__white"
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
            class="bg-zinc-800 rounded-2xl p-6 overflow-hidden text-white lg:mt-36 h-full lg:h-auto animation-show animation-show__dark"
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
    </div>
    <div
      id="benefits"
      class="absolute top-0 lg:top-auto lg:bottom-0 left-0 bg-transparent w-0 h-screen lg:h-[85vh]"
    ></div>
  </section>
</template>

<script setup lang="ts"></script>

<style lang="postcss" scoped>
.animation-show {
  opacity: 0;
  transform: translateY(300px);
  animation: show linear forwards;
}

.animation-show__blue,
.animation-show__orange,
.animation-show__white,
.animation-show__dark {
  animation-timeline: view(80vh 0);
}

@media (min-width: 1024px) {
  .animation-show__blue {
    animation-timeline: view(200vh 50vh);
  }

  .animation-show__orange {
    animation-timeline: view(130vh 75vh);
  }

  .animation-show__white {
    animation-timeline: view(100vh 100vh);
  }

  .animation-show__dark {
    animation-timeline: view(80vh 125vh);
  }
}
@keyframes show {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
