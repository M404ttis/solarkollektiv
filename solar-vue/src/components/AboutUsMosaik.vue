<template>
  <div id="about-us-mosaik-container"
    v-for="asset in aboutUsTexts" :key="asset.text">
        <AboutUsCard v-bind="asset" />
  </div>
</template>

<script lang="ts">
import { aboutUsTexts } from 'src/utils/aboutUsTexts';
import AboutUsCard from './AboutUsCard.vue';
export default {
  name: 'AboutUsMosaik',
  components: {AboutUsCard},
  setup() {
    return {aboutUsTexts};
  },
};
</script>

<style lang="scss" scoped></style>
