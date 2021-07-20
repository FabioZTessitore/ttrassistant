<template>
  <div class="background" :class="{ 'background--turn': turned }">
    <app-light-button v-for="(position, i) in positions" :key="i"
      :left="position.left"
      :top="position.top"
    ></app-light-button>
  The Background
  </div>
</template>

<script>
import LightButton from './LightButton.vue'

export default {
  props: [ 'turned' ],

  data() {
    return {
      positions: [
        { left: '21.5%', top: '84.4%' },    // Barcellona
        { left: '4.3%', top: '86.3%' },     // Lisboa
        { left: '10.8%', top: '82.9%' },    // Madrid
        { left: '10.7%', top: '93.4%' },    // Cadiz
        { left: '20.3%', top: '71.3%' },    // Pamplona
        { left: '34.7%', top: '70.7%' },    // Marseille
        { left: '13.1%', top: '47.3%' },    // Brest
        { left: '26.3%', top: '49.5%' },    // Paris
        { left: '21.6%', top: '43.2%' },    // Dieppe
        { left: '37.4%', top: '57.4%' },    // Zurich
        { left: '29.7%', top: '37.5%' },    // Bruxelles
        { left: '22.7%', top: '30.4%' },    // London
        { left: '31.9%', top: '30.8%' },    // Amsterdam
        { left: '16.4%', top: '9%' },       // Edinburgh
        { left: '39.5%', top: '32.1%' },    // Essen
        { left: '38.1%', top: '42%' },      // Frankfurt
        { left: '49.1%', top: '34.1%' },    // Berlin
        { left: '43.6%', top: '48.4%' },    // Munchen
        { left: '54.5%', top: '50.8%' },    // Wien
        { left: '60%', top: '23%' },        // Danzic
        { left: '45.2%', top: '62.1%' },    // Venezia
        { left: '45.9%', top: '74.8%' },    // Roma
        { left: '49.5%', top: '93.6%' },    // Palermo
        { left: '54.1%', top: '78.5%' },    // Brindisi
        { left: '93.2%', top: '86.3%' },    // Erzurum
        { left: '53.3%', top: '63.8%' },    // Zagrab
        { left: '61.3%', top: '72.2%' },    // Sarajevo
        { left: '65.9%', top: '89.6%' },    // Athina
        { left: '67.7%', top: '73.3%' },    // Sofia
        { left: '74%', top: '93.2%' },      // Smyrna
        { left: '85.6%', top: '89.7%' },    // Angora
        { left: '78.2%', top: '82%' },      // Costantinopoli
        { left: '73.4%', top: '64.2%' },    // Bucuresti
        { left: '86.6%', top: '66.4%' },    // Sevastopoli
        { left: '94.9%', top: '68.5%' },    // Sochi
        { left: '95.5%', top: '55.5%' },    // Rostov
        { left: '91.6%', top: '48.1%' },    // Kharkov
        { left: '78.8%', top: '40.5%' },    // Kyiv
        { left: '59%', top: '54.4%' },      // Budapest
        { left: '64.5%', top: '33%' },      // Warszawa
        { left: '46.4%', top: '17%' },      // Kobenhavn
        { left: '56.2%', top: '6%' },       // Stockholm
        { left: '67.7%', top: '10.1%' },    // Riga
        { left: '83.8%', top: '9.4%' },     // Petrograd
        { left: '93.1%', top: '26.5%' },    // Moskva
        { left: '85%', top: '30%' },        // Smolensk
        { left: '75.2%', top: '29.4%' }     // Wilno
      ]
    }
  },

  components: {
    appLightButton: LightButton,
  }
}
</script>

<style scoped>
.background {
  position: relative;
  aspect-ratio: 3 / 2;
  height: 100vh;
  background: url('../assets/e-board-for-Ticket-to-Ride-Europe.jpg');
  background-size: contain;
  background-repeat: no-repeat;
  margin: 0 auto;
  transition: transform .4s;
}

.background--turn {
  transform: rotate(.5turn);
}
</style>