<template>
  <section
    id="hero"
    class="relative h-screen flex items-center justify-center text-center text-white overflow-hidden scroll-mt-16"
  >
    <!-- Фон -->
    <img
      src="../assets/hero-bg.jpg"
      alt="background"
      class="absolute inset-0 w-full h-full object-cover"
    />
    <div class="absolute inset-0 bg-black/50"></div>

    <!-- Контент -->
    <div class="relative z-10 w-full h-full">
      <!-- Центр: черный бейдж S.SHOTS -->
      <div class="absolute inset-0 flex items-center justify-center pointer-events-none">
        <div class="px-8 py-4 bg-black/80 rounded-2xl shadow-xl">
          <span class="block text-4xl md:text-6xl font-extrabold tracking-widest">
            S.SHOTS
          </span>
        </div>
      </div>

      <!-- Низ: заголовок и подпись -->
      <div class="absolute left-1/2 -translate-x-1/2 bottom-16 md:bottom-24 max-w-3xl w-full px-6">
        <h1 class="text-4xl md:text-6xl font-bold leading-tight drop-shadow-lg">
          Твоя история в кадре
        </h1>
        <p class="mt-4 md:mt-6 text-base md:text-lg text-gray-200 drop-shadow">
          Профессиональная видеосъемка и монтаж. От идеи до готового ролика.
        </p>
      </div>
    </div>
  </section>
</template>
