<template>
  <section
    id="portfolio"
    class="min-h-screen flex flex-col justify-center bg-gray-50 py-20 scroll-mt-16"
  >
    <h2 class="text-4xl font-bold text-center mb-12 text-gray-900">
      Мои работы
    </h2>

    <div class="max-w-6xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-10 px-6">
      <div
        v-for="(work, i) in works"
        :key="i"
        class="flex flex-col rounded-2xl overflow-hidden bg-white shadow-sm ring-1 ring-gray-100 transition-all duration-300 hover:shadow-md hover:-translate-y-0.5"
      >
        <!-- Превью: светло-серый фон -->
        <figure class="group relative w-full bg-gray-200">
          <div class="w-full aspect-[9/16] relative overflow-hidden">
            <!-- Статичный кадр -->
            <img
              :src="work.thumb"
              :alt="work.title"
              class="absolute inset-0 w-full h-full object-cover transition-opacity duration-300 group-hover:opacity-0"
              loading="lazy"
            />
            <!-- GIF при наведении -->
            <img
              :src="work.gif"
              :alt="work.title"
              class="absolute inset-0 w-full h-full object-cover opacity-0 transition-opacity duration-300 group-hover:opacity-100"
              loading="lazy"
            />
          </div>
        </figure>

        <!-- Низ карточки: мягкий светлый градиент, без тёмной полосы -->
        <div
          class="p-6 text-center bg-gradient-to-b from-gray-100/70 to-white border-t border-gray-200"
        >
          <h3 class="text-lg font-semibold mb-2 text-gray-900">
            {{ work.title }}
          </h3>
          <p class="text-sm text-gray-600 mb-4 leading-relaxed">
            {{ work.description }}
          </p>

          <div class="flex justify-center gap-2 flex-wrap">
            <span
              v-for="(tag, t) in work.tags"
              :key="t"
              class="px-3 py-1 rounded-full text-xs bg-gray-100 text-gray-700 border border-gray-200 shadow-[0_0_0_1px_rgba(0,0,0,0.02)]"
            >
              {{ tag }}
            </span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import thumb1 from '../assets/work1.jpg'
import thumb2 from '../assets/work2.jpg'
import thumb3 from '../assets/work3.jpg'

import gif1 from '../assets/work1.gif'
import gif2 from '../assets/work2.gif'
import gif3 from '../assets/work3.gif'

const works = [
  {
    thumb: thumb1,
    gif: gif1,
    title: 'Реклама еды',
    description:
      'Что одновременно может повысить аппетит и продажи? Конечно качественно снятое видео.',
    tags: ['Реклама', 'Рестораны', 'Видеосъемка'],
  },
  {
    thumb: thumb2,
    gif: gif2,
    title: 'Клип для молодёжного комитета',
    description:
      'А мы продолжаем вспоминать как провели День Предпринимателя OPORA SALON - 1 Королевский вечер деловых господ, организованный Молодежным комитетом "ОПОРЫ РОССИИ"',
    tags: ['Музыка', 'Клип', 'Видеосъемка'],
  },
  {
    thumb: thumb3,
    gif: gif3,
    title: 'Едит трофейной BMW',
    description:
      'Трофейная BMW на интерактивной исторической реконструкции в Пскове.',
    tags: ['BMW', 'Псков', 'Видеосъемка'],
  },
]
</script>

<style scoped>
/* плавное переключение фото/gif */
.group img { transition: opacity 0.35s ease; }
@media (prefers-reduced-motion: reduce) {
  .group:hover img { opacity: 1 !important; }
}
</style>
