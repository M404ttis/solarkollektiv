<template>
  <q-page class="items-center justify-evenly">
    <LogoLogo/>
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
import LogoLogo from 'components/LogoLogo.vue'
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'IndexPage',
  components: {
     LogoLogo,
     // EnergyCalculator,
     AboutUsMosaik,
   },
  setup() {
    return { };
  },
});
</script>
