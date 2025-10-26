<template>
  <section
    id="contacts"
    class="min-h-screen flex flex-col justify-center bg-gray-50 py-20 scroll-mt-16"
  >
    <div class="max-w-5xl mx-auto px-6">
      <h2 class="text-4xl font-bold text-center mb-10 text-gray-900">
        Контакты
      </h2>

      <!-- Карточки контактов -->
      <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 mb-10">
        <!-- VK -->
        <a
          :href="vk"
          target="_blank"
          class="rounded-2xl bg-white p-5 shadow-sm ring-1 ring-gray-100 hover:shadow-md transition"
        >
          <div class="text-xl font-semibold text-gray-900">📱 VK</div>
          <div class="text-gray-600 mt-1">@s.shots</div>
        </a>

        <!-- Telegram -->
        <a
          :href="telegram"
          target="_blank"
          class="rounded-2xl bg-white p-5 shadow-sm ring-1 ring-gray-100 hover:shadow-md transition"
        >
          <div class="text-xl font-semibold text-gray-900">✈️ Telegram</div>
          <div class="text-gray-600 mt-1">@AlexanderS3rgeevich</div>
        </a>

        <!-- Instagram -->
        <a
          :href="instagram"
          target="_blank"
          class="rounded-2xl bg-white p-5 shadow-sm ring-1 ring-gray-100 hover:shadow-md transition"
        >
          <div class="text-xl font-semibold text-gray-900">📸 Instagram</div>
          <div class="text-gray-600 mt-1">@alexander.s3rgeevich</div>
        </a>
      </div>

      <!-- Форма заявки -->
      <div
        class="bg-white rounded-2xl shadow-sm ring-1 ring-gray-100 p-6 md:p-8"
      >
        <h3 class="text-2xl font-semibold text-gray-900 mb-6 text-center">
          Расскажите о задаче — я свяжусь с вами
        </h3>

        <form @submit.prevent="submitForm" class="grid grid-cols-1 gap-4">
          <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
            <label class="block">
              <span class="text-sm text-gray-600">Ваше имя</span>
              <input
                v-model.trim="form.name"
                type="text"
                required
                placeholder="Иван"
                class="mt-1 w-full rounded-xl border border-gray-300 bg-white px-4 py-3 outline-none focus:border-gray-400"
              />
            </label>

            <label class="block">
              <span class="text-sm text-gray-600">Телефон или Telegram</span>
              <input
                v-model.trim="form.phone"
                type="text"
                required
                placeholder="+7 900 000-00-00 / @username"
                class="mt-1 w-full rounded-xl border border-gray-300 bg-white px-4 py-3 outline-none focus:border-gray-400"
              />
            </label>
          </div>

          <label class="block">
            <span class="text-sm text-gray-600">Комментарий</span>
            <textarea
              v-model.trim="form.message"
              rows="4"
              placeholder="Коротко опишите задачу: формат, сроки, площадки…"
              class="mt-1 w-full rounded-xl border border-gray-300 bg-white px-4 py-3 outline-none focus:border-gray-400"
            ></textarea>
          </label>

          <div class="flex items-center justify-between flex-wrap gap-3">
            <p class="text-sm text-gray-500">
              Работаю в Пскове и области. Отвечаю обычно в тот же день.
            </p>
            <button
              type="submit"
              class="inline-flex items-center justify-center rounded-xl px-6 py-3 bg-gray-900 text-white font-medium hover:bg-gray-800 transition shadow-sm"
            >
              Отправить
            </button>
          </div>
        </form>
      </div>
    </div>
  </section>
</template>

<script setup>
import { reactive } from 'vue'

// 🔗 ссылки на соцсети
const vk = 'https://vk.com/s.shots'
const telegram = 'https://t.me/AlexanderS3rgeevich'
const instagram = 'https://instagram.com/alexander.s3rgeevich'
const EMAIL = 's.shots@example.com' // замени на реальный email

const form = reactive({
  name: '',
  phone: '',
  message: '',
})

function submitForm() {
  const subject = `Заявка с сайта: ${form.name}`
  const body =
    `Имя: ${form.name}\n` +
    `Контакт: ${form.phone}\n\n` +
    `Комментарий:\n${form.message || '-'}`

  const url = `mailto:${EMAIL}?subject=${encodeURIComponent(
    subject
  )}&body=${encodeURIComponent(body)}`
  window.location.href = url
}
</script>
