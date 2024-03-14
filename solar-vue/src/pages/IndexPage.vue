<template>
  <q-page class="items-center justify-evenly">
    <AboutUsMosaik/>
    <!-- <AboutUsCarousel /> -->
    <EnergyCalculator/>
  </q-page>
</template>

<script lang="ts">
// import { Todo, Meta } from 'components/models';
// import AboutUsCarousel from 'components/AboutUsCarousel.vue';
import EnergyCalculator from 'components/EnergyCalculator.vue';
import AboutUsMosaik from 'components/AboutUsMosaik.vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'IndexPage',
  components: { 
      // AboutUsCarousel, 
      EnergyCalculator, 
      AboutUsMosaik
   },
  setup() {
    return { };
  },
});
</script>
