<template>
  <footer class="bg-[var(--bg-card)] text-[var(--text-secondary)] py-10 px-4 mt-10 border-t border-[var(--border-color)]">
    <div class="max-w-5xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-8 text-center md:text-left">
      
      <div>
        <h3 class="text-[var(--text-main)] font-bold text-lg mb-4">BetWins</h3>
        <p class="text-sm">
          Ваш надежный партнер в мире спортивных ставок. Мы предлагаем лучшие коэффициенты и захватывающий опыт для каждого фаната спорта.
        </p>
        <div class="flex justify-center md:justify-start gap-4 mt-4">
          <a href="#" class="text-[var(--text-secondary)] hover:text-[var(--accent-primary)] transition-colors">
            <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0c-6.627 0-12 5.373-12 12s5.373 12 12 12 12-5.373 12-12-5.373-12-12-12zm-2 16h-2v-6h2v6zm-1-7.75c-.69 0-1.25-.56-1.25-1.25s.56-1.25 1.25-1.25 1.25.56 1.25 1.25-.56 1.25-1.25 1.25zm11 7.75h-2v-4.5c0-.966-.026-2.22-.057-3.238-.061-1.921-1.517-3.182-3.661-3.182-1.859 0-3.085 1.218-3.628 2.385v-2.025h-2s.027 5.518 0 6h2v-3.723c0-.923.066-1.821.196-2.46.368-1.848 1.956-2.483 3.033-2.483 1.077 0 1.905.374 2.193 1.134.331.868.225 1.97.225 3.328v3.704z"/></svg>
          </a>
          <a href="#" class="text-[var(--text-secondary)] hover:text-[var(--accent-primary)] transition-colors">
             <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M22.28 6.07c-.43.19-.89.32-1.37.38a4.95 4.95 0 0 0 2.16-1.32 9.94 9.94 0 0 1 -1.55.59 4.95 4.95 0 0 0 -8.44 4.5 14.04 14.04 0 0 1 -10.21-5.18 4.95 4.95 0 0 0 1.53 6.6 4.92 4.92 0 0 1 -2.23-.62v.06a4.95 4.95 0 0 0 3.97 4.85 4.98 4.98 0 0 1 -2.23.08 4.95 4.95 0 0 0 4.61 3.44 9.97 9.97 0 0 1 -6.15 2.12c-.4 0-.8-.02-1.19-.06a14.04 14.04 0 0 0 7.57 2.21c9.08 0 14.03-7.51 14.03-14.03l-.01-.64a10.05 10.05 0 0 0 2.46-2.55z"/></svg>
          </a>
          </div>
      </div>
      
      <div>
        <h3 class="text-[var(--text-main)] font-bold text-lg mb-4">Навигация</h3>
        <ul class="space-y-2 text-sm">
          <li><a href="#" class="hover:text-[var(--accent-primary)] transition-colors">Главная</a></li>
          <li><a href="#" class="hover:text-[var(--accent-primary)] transition-colors">О нас</a></li>
          <li><a href="#" class="hover:text-[var(--accent-primary)] transition-colors">Виды спорта</a></li>
          <li><a href="#" class="hover:text-[var(--accent-primary)] transition-colors">Правила</a></li>
          <li><a href="#" class="hover:text-[var(--accent-primary)] transition-colors">FAQ</a></li>
        </ul>
      </div>

      <div>
        <h3 class="text-[var(--text-main)] font-bold text-lg mb-4">Свяжитесь с нами</h3>
        <ul class="space-y-2 text-sm">
          <li>Email: <a href="mailto:support@betwins.com" class="hover:text-[var(--accent-primary)] transition-colors">support@betwins.com</a></li>
          <li>Телефон: <a href="tel:+1234567890" class="hover:text-[var(--accent-primary)] transition-colors">+1 (234) 567-890</a></li>
          <li>Адрес: Примерная ул., 123, Город, Страна</li>
          <li><a href="#" class="hover:text-[var(--accent-primary)] transition-colors">Политика конфиденциальности</a></li>
          <li><a href="#" class="hover:text-[var(--accent-primary)] transition-colors">Условия использования</a></li>
        </ul>
      </div>
    </div>

    <div class="text-center text-sm mt-10 pt-6 border-t border-[var(--border-color)]">
      &copy; {{ new Date().getFullYear() }} BetWins. Все права защищены.
    </div>
  </footer>
</template>