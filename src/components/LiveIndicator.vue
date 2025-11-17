<template>
  <div class="flex items-center gap-2">
    <!-- Мигающая точка -->
    <span
      class="inline-block w-3 h-3 rounded-full bg-[var(--accent-primary)] animate-pulse"
    ></span>

    <!-- LIVE текст -->
    <span class="text-[var(--accent-primary)] font-semibold tracking-wide">
      LIVE
    </span>
  </div>
</template>

<style scoped>
@keyframes pulseStrong {
  0% { opacity: 1; transform: scale(1); }
  50% { opacity: 0.4; transform: scale(0.85); }
  100% { opacity: 1; transform: scale(1); }
}

.animate-pulse {
  animation: pulseStrong 1.2s infinite ease-in-out;
}
</style>
