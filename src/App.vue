<script setup>
import { ref } from 'vue';

import Header from './components/Header.vue'
import GameEventCard from './components/GameEventCard.vue'
import LiveIndicator from './components/LiveIndicator.vue';
import RegistrationModal from './components/RegistrationModal.vue';
import Footer from './components/Footer.vue';
import BenefitsSection from './components/BenefitsSection.vue';
import ExpertiseSection from './components/ExpertiseSection.vue';

// Реактивная переменная для управления видимостью модального окна
const showModal = ref(false);

// Функция-обработчик клика
const openRegistrationModal = () => {
  showModal.value = true;
};

</script>

<template>
  <div class="main-background" >
    <Header />
      <main class="flex-1 py-10 px-4" data-aos="fade-up">

        <BenefitsSection/>

        <div class="main-content-wrapper max-w-5xl mx-auto bg-[var(--bg-card)] rounded-2xl p-8 border-1 border-[var(--border-color)] space-y-4 shadow-custom-glow">
          
          <h1 class="text-[var(--text-main)] text-center text-3xl md:text-4xl font-extrabold mb-4 leading-tight">
            Твой первый <span class="text-[var(--accent-primary)]">КРУПНЫЙ ВЫИГРЫШ</span> ждет!
          </h1>
          
          <h2 class="text-[var(--text-secondary)] text-xl text-center font-medium">
            Начни без риска: получи БЕСПЛАТНЫЙ фрибет <span class="text-white font-bold">15 000 ₽</span> прямо сейчас!
          </h2>

          <div class="flex justify-center pt-2">
            <button
              id='CTA'
              class="bg-[var(--accent-primary)] text-[var(--bg-card)] font-bold text-lg px-8 py-3 rounded-xl hover:opacity-90 transition-opacity duration-200 cursor-pointer shadow-lg shadow-[var(--accent-primary)]/40"
              @click="openRegistrationModal" >
              Забрать Фрибет и начать выигрывать!
            </button>
          </div>

          <GameEventCard
            @click="openRegistrationModal"
            teamA="Real Madrid"
            teamB="Barcelona"
            coef1="1.85"
            draw="3.40"
            coef2="4.20"
            date="21.07"
            time="19:00"
            league="LaLiga"
            countryCodeA="ES"  
            countryCodeB="ES"
          >
            <template #live>
              <LiveIndicator />
            </template>
          </GameEventCard>

          <GameEventCard
            @click="openRegistrationModal"
            teamA="Bayern"
            teamB="Borussia"
            coef1="1.65"
            draw="3.90"
            coef2="5.10"
            date="22.07"
            time="21:00"
            league="Bundesliga"
            countryCodeA="DE"
            countryCodeB="DE"
          >
            <template #live>
              <LiveIndicator />
            </template>
          </GameEventCard>

          <GameEventCard
            @click="openRegistrationModal"
            teamA="Manchester City"
            teamB="Liverpool"
            coef1="2.10"
            draw="3.50"
            coef2="3.60"
            date="23.07"
            time="20:45"
            league="Premier League"
            countryCodeA="GB"
            countryCodeB="GB"
          >
            <template #live>
              <LiveIndicator />
            </template>
          </GameEventCard>

          <GameEventCard
            @click="openRegistrationModal"
            teamA="Juventus"
            teamB="Inter Milan"
            coef1="2.40"
            draw="3.10"
            coef2="2.95"
            date="24.07"
            time="22:00"
            league="Serie A"
            countryCodeA="IT"
            countryCodeB="IT"
          >
            <template #live>
              <LiveIndicator />
            </template>
          </GameEventCard>

          <GameEventCard
            @click="openRegistrationModal"
            teamA="PSG"
            teamB="Marseille"
            coef1="1.55"
            draw="4.00"
            coef2="5.20"
            date="25.07"
            time="21:00"
            league="Ligue 1"
            countryCodeA="FR"
            countryCodeB="FR"
          >
            <template #live>
              <LiveIndicator />
            </template>
          </GameEventCard>

          <GameEventCard
            @click="openRegistrationModal"
            teamA="Bayern"
            teamB="Borussia Dortmund"
            coef1="1.65"
            draw="3.90"
            coef2="5.10"
            date="22.07"
            time="21:00"
            league="Bundesliga"
            countryCodeA="DE"
            countryCodeB="DE"
          >
            <template #live>
              <LiveIndicator />
            </template>
          </GameEventCard>
        </div>

        <ExpertiseSection/>

      </main>
    <Footer />
  </div>
    
    <RegistrationModal :visible="showModal" @close="showModal = false" />
</template>

<style>
.main-background {
  background-image: url('./assets/background.png'); 
  background-size: cover;
  background-attachment: scroll; 
  background-position: center center;
  background-position: 50% 50%;
  min-height: 100vh;
  animation: backgroundPan 30s infinite alternate linear;
}

@keyframes backgroundPan {
  0% { background-position: 55% 45%; }
  100% { background-position: 45% 55%; }
}

.shadow-custom-glow {
  box-shadow: 
        0 4px 6px -1px rgba(0, 0, 0, 0.1), 
        0 2px 4px -2px rgba(0, 0, 0, 0.1),
        0 0 40px -5px rgba(15, 186, 129, 0.4); 
}
</style>