<template>
  <div id="about-us-card">
    <q-card class="q-ma-md q-pa-sm">
      <h4 class="q-mb-md">{{ title }}</h4>
      <p class="q-ma-xs">
        {{ text }}
      </p>
    </q-card>
  </div>
</template>

<script lang="ts">
export default {
  name: 'AboutUsCard',
  components: {},
  props: {
    title: {
      type: String,
      required: true,
    },

    text: {
      type: String,
      required: true,
    },
  },
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped></style>
