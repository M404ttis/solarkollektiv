<template>
  <q-page class="row items-center justify-evenly">
    <q-carousel
      v-model="slide"
      transition-prev="scale"
      transition-next="scale"
      swipeable
      animated
      control-color="$secondary"
      navigation
      padding
      arrows
      height="50vh"
      class="bg-secondary"
    >
      <q-carousel-slide
        v-for="text in aboutUsTexts"
        :key="text.title"
        v-bind="text"
        :name="text.title"
      >
        <q-icon :name="text.icon" class="column no-wrap flex-center" />
        <div class="q-mt-md text-center">
          {{ text.text }}
        </div>
      </q-carousel-slide>
    </q-carousel>
  </q-page>
</template>

<script lang="ts">
// import { Todo, Meta } from 'components/models';
import { defineComponent, ref } from 'vue';
import { aboutUsTexts } from '../utils/aboutUsTexts';

export default defineComponent({
  name: 'AboutUsCarousel',
  components: {},
  setup() {
    let slide = ref(null);
    return { slide, aboutUsTexts };
  },
});
</script>
