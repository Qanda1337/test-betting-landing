<template>
  <header class="cursor-pointer bg-[var(--bg-card)]/0 w-full h-10 flex items-center justify-between px-[17%]">
    <!-- Логотип / название -->
    <h1 class="text-[var(--text-main)] text-2xl font-bold">BetWins</h1>

    <!-- Кнопка Log In -->
    <button
      class="bg-[var(--accent-primary)] text-[var(--bg-card)] font-semibold px-4 py-0.5 rounded-lg hover:bg-[var(--accent-secondary)] transition-colors duration-200 cursor-pointer"
      @click="showModal = true"
    >
      Log In
    </button>

    <!-- Модальное окно -->
    <RegistrationModal :visible="showModal" @close="showModal = false" />
  </header>
</template>

<script setup>
import { ref } from 'vue'
import RegistrationModal from './RegistrationModal.vue'

const showModal = ref(false)
</script>