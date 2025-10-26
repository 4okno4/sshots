<template>
  <section
    id="about"
    class="min-h-screen flex flex-col justify-center items-center bg-gray-50 py-20 scroll-mt-16"
  >
    <div class="max-w-5xl mx-auto px-6 text-center">
      <h2 class="text-4xl font-bold mb-10 text-gray-900">Обо мне</h2>

      <div
        class="flex flex-col md:flex-row items-center gap-10 bg-white p-8 rounded-2xl shadow-sm ring-1 ring-gray-100"
      >
        <!-- Фото -->
        <div class="w-full md:w-1/3 flex justify-center">
          <img
            src="../assets/about-photo.jpg"
            alt="S.SHOTS автор"
            class="rounded-2xl object-cover shadow-md w-64 h-64 md:w-80 md:h-80"
          />
        </div>

        <!-- Текст -->
        <div class="md:w-2/3 text-left text-gray-700 space-y-4 leading-relaxed">
          <p class="text-lg font-medium text-gray-900">
            👋 Привет, я Александр
          </p>
          <p>
            Помогу показать <strong>вашу историю</strong>!
          </p>
          <p>
            🎥 Профессиональная видеосъемка и монтаж в <strong>Пскове</strong>.
            Сделаем качественное и эмоциональное видео, которое сохранит ваши
            лучшие моменты на долгие годы.
          </p>
          <p>
            Работаю в <strong>Пскове и области</strong>. Индивидуальный подход
            под вашу задачу, быстрые сроки выполнения работ.
          </p>

          <div class="pt-2">
            <h3 class="text-xl font-semibold text-gray-900 mb-3">
            📽️ Предоставляемые услуги:
            </h3>
            <ul class="list-disc list-inside space-y-1 text-gray-700">
              <li>
                Съёмка рекламных роликов для бизнеса в любом формате;
              </li>
              <li>
                Продвигающие видео для социальных сетей
                <span class="italic">(Reels, YouTube)</span>;
              </li>
              <li>
                Съёмка танцевальных клипов
                <span class="italic">(постановочная хореография, селекты)</span>;
              </li>
              <li>
                Монтаж видеороликов из <strong>ваших</strong> исходников.
              </li>
            </ul>
          </div>

          <!-- CTA -->
          <div class="pt-6">
            <a
              href="#contacts"
              class="inline-flex items-center justify-center rounded-xl px-6 py-3 bg-gray-900 text-white font-medium hover:bg-gray-800 transition shadow-sm"
            >
              Обсудить проект
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
