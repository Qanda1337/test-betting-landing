<template>
  <div
    class="cursor-pointer bg-[var(--bg-card)] border border-[var(--border-color)] rounded-xl p-4 flex flex-col gap-3 shadow-lg hover:border-[var(--accent-primary)] transition-colors duration-200"
    @click="showModal = true"
    data-aos="fade-up"
  >
    <slot name="live"></slot>

    <div class="grid grid-cols-3 items-center">
    
    <div class="flex items-center gap-2">
        <span v-if="countryCodeA" class="text-2xl">{{ getFlagEmoji(countryCodeA) }}</span>
        <div class="flex flex-col">
            <span class="text-[var(--text-main)] font-semibold text-lg">{{ teamA }}</span>
            <span class="text-[var(--text-secondary)] text-sm">{{ league }}</span>
        </div>
    </div>

    <div class="text-center text-[var(--text-main)] text-sm font-semibold">
        {{ time }}
    </div>

    <div class="flex items-center justify-end gap-2">
        <div class="flex flex-col text-right">
            <span class="text-[var(--text-main)] font-semibold text-lg">{{ teamB }}</span>
            <span class="text-[var(--text-secondary)] text-sm">{{ date }}</span>
        </div>
        <span v-if="countryCodeB" class="text-2xl">{{ getFlagEmoji(countryCodeB) }}</span>
    </div>

    </div>

    <div class="h-px bg-[var(--border-color)]"></div>

    <div class="grid grid-cols-3 gap-3 text-center">
      <button
        class="cursor-pointer bg-[var(--bg-card)] border border-[var(--border-color)] rounded-lg p-3 hover:border-[var(--accent-primary)] transition"
      >
        <span class="block text-[var(--text-secondary)] text-sm">П1</span>
        <span class="block text-[var(--text-main)] text-lg font-bold">{{ coef1 }}</span>
      </button>

      <button
        class="cursor-pointer bg-[var(--bg-card)] border border-[var(--border-color)] rounded-lg p-3 hover:border-[var(--accent-primary)] transition"
      >
        <span class="block text-[var(--text-secondary)] text-sm">X</span>
        <span class="block text-[var(--text-main)] text-lg font-bold">{{ draw }}</span>
      </button>

      <button
        class="cursor-pointer bg-[var(--bg-card)] border border-[var(--border-color)] rounded-lg p-3 hover:border-[var(--accent-primary)] transition"
      >
        <span class="block text-[var(--text-secondary)] text-sm">П2</span>
        <span class="block text-[var(--text-main)] text-lg font-bold">{{ coef2 }}</span>
      </button>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

defineProps({
  teamA: String,
  teamB: String,
  coef1: [String, Number], 
  draw: [String, Number],
  coef2: [String, Number],
  time: String,
  date: String,
  league: String,
  countryCodeA: String,
  countryCodeB: String,
});

const showModal = ref(false)


// Функция для конвертации кода страны (например, 'ES') в эмодзи флага
const getFlagEmoji = (countryCode) => {
  if (!countryCode) return '';
  // Использует Региональные индикаторные символы (Regional Indicator Symbols)
  const codePoints = countryCode
    .toUpperCase()
    .split('')
    .map(char => 127397 + char.charCodeAt());
  return String.fromCodePoint(...codePoints);
};
</script>