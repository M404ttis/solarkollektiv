<template>
  <div class="bg-primary text-white font-size">
    <div class="column justify-start items-center text-weigth-light text-caption" >
      <span> Solarkollektiv Gmbh </span>
      <span> Werner-Heisenberg-Straße </span>
      <span> 39106 Magdeburg </span>
      <span> 0391 5576 0026 </span>
      <span>  info(at)solarkollektiv.eu </span>
      <div @click="router.push('impressum')">impressum</div>
    </div>
  </div>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';
  import {useRouter} from 'vue-router'

  export default defineComponent({
      name:'FooterSimple',
      components: {},
      setup() {
        const router = useRouter();
      return{router };
      }
    })
</script>
<style>
 span{margin: 0 0.2em}
</style>
