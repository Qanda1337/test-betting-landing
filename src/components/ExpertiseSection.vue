<template>
  <div class="max-w-5xl mx-auto py-12 px-4" data-aos="fade-up">
    
    <h2 class="text-3xl font-bold text-[var(--text-main)] text-center mb-10">
      Инновации в ставках: <span class="text-[var(--accent-primary)]">Наша Экспертиза</span>
    </h2>

    <div class="bg-[var(--bg-card)] p-8 rounded-2xl border border-[var(--border-color)] shadow-custom-glow flex flex-col lg:flex-row items-center gap-8">
      
      <div class="lg:w-1/2 text-center lg:text-left">
        <h3 class="text-[var(--text-main)] text-2xl font-semibold mb-4">
          Предиктивная аналитика на основе AI
        </h3>
        <p class="text-[var(--text-secondary)] mb-4">
          Мы используем передовые алгоритмы машинного обучения для анализа тысяч данных в секунду. Это позволяет нам предлагать вам не просто коэффициенты, а информированные прогнозы.
        </p>
        <ul class="space-y-2 text-[var(--text-secondary)] text-sm list-disc list-inside">
          <li>Анализ формы игроков и травм</li>
          <li>Моделирование исходов матчей в реальном времени</li>
          <li>Нейронные сети для выявления "валуев"</li>
        </ul>
      </div>

      <div class="lg:w-1/2 w-full h-64 bg-[var(--bg-main)] rounded-lg p-4 relative overflow-hidden">
        <div class="flex justify-between text-xs text-[var(--text-secondary)] mb-2">
            <span>Прогнозы на 7 дней</span>
            <span class="text-[var(--accent-primary)] font-bold">+12% точности</span>
        </div>
        
        <div class="flex items-end h-48 gap-1 border-b border-[var(--border-color)] pt-2">
          <div class="w-1/6 h-full flex flex-col justify-end">
            <div class="bg-blue-600 rounded-t-sm h-[30%] opacity-70"></div>
          </div>
          <div class="w-1/6 h-full flex flex-col justify-end">
            <div class="bg-blue-600 rounded-t-sm h-[50%] opacity-70"></div>
          </div>
          <div class="w-1/6 h-full flex flex-col justify-end">
            <div class="bg-[var(--accent-primary)] rounded-t-sm h-[80%]"></div>
          </div>
          <div class="w-1/6 h-full flex flex-col justify-end">
            <div class="bg-blue-600 rounded-t-sm h-[40%] opacity-70"></div>
          </div>
          <div class="w-1/6 h-full flex flex-col justify-end">
            <div class="bg-blue-600 rounded-t-sm h-[65%] opacity-70"></div>
          </div>
          <div class="w-1/6 h-full flex flex-col justify-end">
            <div class="bg-blue-600 rounded-t-sm h-[75%] opacity-70"></div>
          </div>
        </div>
        <span class="absolute bottom-1 right-4 text-[var(--text-secondary)] text-xs">AI Powered</span>
      </div>
    </div>
  </div>
</template>