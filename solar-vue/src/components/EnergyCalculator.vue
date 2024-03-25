<template >
  <div class="q-pa-md ">
    <q-card id="calculator-wrapper"
      class="q-pa-md "
    >
    <h6 class="q-my-md ">Einsparpotential Errechnen</h6>
      <q-form
        @submit="onSubmit"
        @reset="onReset"
        class="q-gutter-md ">

        <q-input
          filled
          v-model="roofSize"
          label="Dachfläche in quadratmetern"
          hint="Bsp.: 5"
          lazy-rules
        />

        <q-input
          filled
          v-model="roofDirection"
          label="Ausrichtung des Daches"
          hint="Bsp.: 5"
          lazy-rules
        />

        <div id="form-button-container" class="row justify-between">
          <q-btn label="Berechnen" type="submit" class="bg-secondary" color="primary"/>
          <q-btn label="Löschen" type="reset" color="bg-primary" flat class="q-ml-sm" />
        </div>
      </q-form>
    </q-card>
  </div>
</template>

<script lang="ts">
import { ref, defineComponent } from 'vue'
import { useQuasar } from 'quasar'
export default defineComponent({
    name: 'EnergyCalculator',
    components:{},
    setup() {
      const $q = useQuasar()

      const roofSize = ref(null)
      const roofDirection = ref('')


      const onSubmit = () => {

        if (roofSize.value === null) {
          $q.notify({
            color: 'red-5',
            textColor: 'white',
            icon: 'warning',
            message: 'Die Dachgröße ist zur Berechnung notwendig!'
          })
        } else if (roofDirection.value === '') {

        } else {
          $q.notify({
            color: '$primary',
            textColor: '$secondary',
            icon: '☀️',
            message: 'super, lass uns ansehen, was das energetisch heißt!'
          })

        }

      };

      const onReset = () => {
        roofSize.value = null
        roofDirection.value = '';
        }

      return{roofSize, roofDirection, onSubmit, onReset}
    }
})

</script>
<style lang="scss">

</style>
