<template>
  <header class="cursor-pointer bg-[var(--bg-card)]/0 w-full h-10 flex items-center justify-between px-[17%]">
    <h1 class="text-[var(--text-main)] text-2xl font-bold">BetWins</h1>

    <button
      class="bg-[var(--accent-primary)] text-[var(--bg-card)] font-semibold px-4 py-0.5 rounded-lg hover:bg-[var(--accent-secondary)] transition-colors duration-200 cursor-pointer"
      @click="showModal = true"
    >
      Log In
    </button>

    <RegistrationModal :visible="showModal" @close="showModal = false" />
  </header>
</template>

<script setup>
import { ref } from 'vue'
import RegistrationModal from './RegistrationModal.vue'

const showModal = ref(false)
</script>