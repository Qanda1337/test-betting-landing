<script setup>
import { ref } from 'vue';

import Header from './components/Header.vue'
import GameEventCard from './components/GameEventCard.vue'
import LiveIndicator from './components/LiveIndicator.vue';
import RegistrationModal from './components/RegistrationModal.vue';
import Footer from './components/Footer.vue';

// Реактивная переменная для управления видимостью модального окна
const showModal = ref(false);

// Функция-обработчик клика
const openRegistrationModal = () => {
  showModal.value = true;
};

</script>

<template>
  <Header />
    <main class="flex-1 py-10 px-4" data-aos="fade-up">
      <div class="max-w-5xl mx-auto bg-[var(--bg-card)] rounded-2xl p-8 shadow-xxl border-1 border-[var(--border-color)] space-y-4">
        
        <h1 class="text-[var(--text-main)] text-center">Сделай свою первую ставку на спорт, используя фрибет 15.0000p!</h1>

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
    </main>

  <Footer />
    
    <RegistrationModal :visible="showModal" @close="showModal = false" />
</template>