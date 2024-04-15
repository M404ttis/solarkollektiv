<template>
  <div class="column justify-start items-start">

    <span>
      Angaben gemäß § 5 TMG
    </span>

    <div class="column justify-start items-start">
      <h5>Anschrift</h5>
      <span>Solarkollektiv GmbH</span>
      <span>Werner-Heisenberg-Straße 3</span>
      <span>39106 Magdeburg</span>
    </div>


    <div class="column justify-start items-start">
      <span>Handelsregister: HRB 31940</span>
      <span>Registergericht: Stendal</span>
    </div>

    <div class="column justify-start items-start">
      <span>Vertreten durch:</span>
      <span>Nils Fokuhl & Hannes Kühn</span>
    </div>


    <div class="column justify-start items-start">
      <h5>Kontakt</h5>
      <span>Telefon: +49 391 5576 0026 </span>
      <span>Telefax: +49 391 5576 0023 </span>
      <span>E-Mail: info[at]solarkollektiv.eu </span>
    </div>

    <div class="column justify-start items-start">
      <h5>Umsatzsteuer-ID</h5>
      <span>Umsatzsteuer-Identifikationsnummer gemäß §27a Umsatzsteuergesetz:</span>
      <span>DE357337685</span>
    </div>


    <div class="column justify-start items-start">
      <h5>EU-Streitschlichtung</h5>
      <span>Die Europäische Kommission stellt eine Plattform zur Online-Streitbeilegung (OS) bereit:</span>
      <span>https://ec.europa.eu/consumers/odr/</span>
      <span>Unsere E-Mail-Adresse finden Sie oben im Impressum.</span>
    </div>

    <div class="column justify-start items-start">
      <h5>Verbraucherstreitbeilegung/Universalschlichtungsstelle</h5>
      <span>Wir sind nicht bereit oder verpflichtet, an Streitbeilegungsverfahren vor einer Verbraucherschlichtungsstelle teilzunehmen.</span>
    </div>

  </div>
</template>

<script lang="ts">
  import {defineComponent} from 'vue'

  export default
     defineComponent({
      name: 'ImpressumPage',
      components: {},
      setup(){ return{};}
    })
</script>

<style lang="scss">
  div, h5{margin: 0.5rem 0.2rem}
</style>
