<template>
  <q-page class="items-center justify-evenly">
    <LogoLogo/>
    <MissionStatement/>
    <AboutUsMosaik/>
    <!-- <AboutUsCarousel /> -->
    <!-- <EnergyCalculator/> -->
  </q-page>
</template>

<script lang="ts">
// import { Todo, Meta } from 'components/models';
// import AboutUsCarousel from 'components/AboutUsCarousel.vue';
import EnergyCalculator from 'components/EnergyCalculator.vue';
import AboutUsMosaik from 'components/AboutUsMosaik.vue';
import LogoLogo from 'components/LogoLogo.vue';
import MissionStatement from 'components/MissionStatement.vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'IndexPage',
  components: {
     LogoLogo,
    MissionStatement,
     // EnergyCalculator,
     AboutUsMosaik,
   },
  setup() {
    return { };
  },
});
</script>
