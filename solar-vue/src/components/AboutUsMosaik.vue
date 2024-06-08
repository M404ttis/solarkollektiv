<template>
  <div id="about-us-mosaik-container" class="row justify-center" >
        <AboutUsCard class="col-xs-12 col-sm-10 col-md-8 col-lg-8" v-for="asset in aboutUsTexts" :key="asset.text" v-bind="asset" />
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

<style lang="scss" scoped>
// if small screen, flex in row
@media (max-width: 600px){
  #about-us-mosaik-container{
    display: grid;
    flex-direction: column;
    justify-content: center;
  }
}


// if larger screen, display side by side
/*
@media (min-width: 601px){
  #about-us-mosaik-container{
    display: grid;
    flex-direction: row;
    justify-content: center;
  }
}
  */
</style>
