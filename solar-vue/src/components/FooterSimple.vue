<template>
  <div>
    <a href="../pages/Impressum.vue">impressum</a>
    <span> Made with love and vue.js in Berlin </span>
    <p>
      Solarkollektiv Gmbh
      Werner-Heisenberg-Straße 3
      39106 Magdeburg
      0391 5576 0026
      info(at)solarkollektiv.eu
    </p>
  </div>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';

  export default defineComponent({
      name:'FooterSimple',
      components: {},
      setup() {return{};
      }
    })
</script>
