<template>
  <q-footer class="bg-tertiary">
    <q-toolbar class="column flex-center ">
      <div class="column flex-center text-weigth-light text-caption" >
        <span> Solarkollektiv GmbH </span>
        <span> Werner-Heisenberg-Straße </span>
        <span> 39106 Magdeburg </span>
        <span> 0391 5576 0026 </span>
        <span>  info(at)solarkollektiv.eu </span>
        <a @click="router.push('impressum')">impressum</a>
      </div>
    </q-toolbar>
  </q-footer>
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

 a{text-decoration: underline;}

</style>
