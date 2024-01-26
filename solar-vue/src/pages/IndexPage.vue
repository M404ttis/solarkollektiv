<template>
  <q-page class="row items-center justify-evenly">
    <AboutUsCarousel />
  </q-page>
</template>

<script lang="ts">
// import { Todo, Meta } from 'components/models';
import AboutUsCarousel from 'components/AboutUsCarousel.vue';
import { defineComponent, ref } from 'vue';
import { aboutUsTexts } from '../utils/aboutUsTexts';

export default defineComponent({
  name: 'IndexPage',
  components: { AboutUsCarousel },
  setup() {
    return { AboutUsCarousel, aboutUsTexts };
  },
});
</script>
