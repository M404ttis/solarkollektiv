<template>
    <q-carousel
      v-model="slide"
      transition-prev="scale"
      transition-next="scale"
      swipeable
      infinite
      animated
      control-color="$secondary"
      navigation
      padding
      arrows
      class="bg-secondary rounded-borders q-ma-md column "
    >

      <q-carousel-slide
        v-for="text in aboutUsTexts"
        :key="text.title"
        v-bind="text"
        :name="text.title"
        class="row flex-center"
      >

      <!-- <q-icon :name="text.icon" class="column no-wrap flex-center" /> -->
          <h4 class="q-mb-sm">{{text.title}}</h4>
        <div class="q-mt-md text-center">
          {{ text.text }}
        </div>
      </q-carousel-slide>
    </q-carousel>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import { aboutUsTexts } from '../utils/aboutUsTexts';

export default defineComponent({
  name: 'AboutUsCarousel',
  components: {},
  setup() {
    const slide = ref(2);
    return { slide, aboutUsTexts };
  },
});
</script>
