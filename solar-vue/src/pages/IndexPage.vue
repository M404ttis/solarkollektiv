<template>
  <q-page class="row items-center justify-evenly">
    <AboutUsCard v-for="text in aboutUsTexts" :key="text.title" v-bind="text" />
  </q-page>
</template>

<script lang="ts">
// import { Todo, Meta } from 'components/models';
import AboutUsCard from 'components/AboutUsCard.vue';
import { defineComponent, ref } from 'vue';
import { aboutUsTexts } from '../utils/aboutUsTexts';

export default defineComponent({
  name: 'IndexPage',
  components: { AboutUsCard },
  setup() {
    return { AboutUsCard, aboutUsTexts };
  },
});
</script>
