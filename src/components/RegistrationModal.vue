<template>
  <div
    v-if="visible"
    class="fixed inset-0 z-50 flex items-center justify-center bg-black/50"
    @click.self="$emit('close')"
  >
    <!-- Модальное окно -->
    <div
      class="bg-[var(--bg-card)] rounded-2xl p-8 max-w-md w-full shadow-xl relative"
      data-aos="fade-up"
      data-aos-duration="400"
      data-aos-offset="100"
    >
      <!-- Кнопка закрытия -->
      <button
        class="absolute top-4 right-4 text-[var(--text-secondary)] hover:text-[var(--accent-primary)]"
        @click="$emit('close')"
      >
        ✕
      </button>

      <!-- Заголовок -->
      <h2 class="text-[var(--accent-primary)] font-bold text-xl mb-6 text-center">
        Получи Фрибет до 15.000р за регистрацию прямо сейчас!
      </h2>

      <!-- Поле ввода -->
      <input
        type="tel"
        placeholder="Введите номер телефона"
        class="w-full p-3 rounded-lg bg-[var(--bg-main)] border border-[var(--border-color)] text-[var(--text-main)] placeholder-[var(--text-secondary)] mb-4 focus:outline-none focus:border-[var(--accent-primary)] transition-colors"
      />

      <!-- Кнопка Зарегистрироваться -->
      <button
        class="w-full bg-[var(--accent-primary)] text-[var(--bg-card)] font-semibold py-3 rounded-lg hover:bg-[var(--accent-secondary)] transition-colors"
      >
        Зарегистрироваться
      </button>
    </div>
  </div>
</template>

<script setup>
defineProps({
  visible: Boolean
})
</script>
