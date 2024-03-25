<template>
  <div id="about-us-card ">

    <q-card class="my-card q-ma-md">
      <q-img :src=imgUrl>
        <div class="absolute-bottom text-h6">
          {{title}}
        </div>
      </q-img>

      <q-card-section>
        {{ text }}
      </q-card-section>
    </q-card>

  </div>
</template>

<script lang="ts">
export default {
  name: 'AboutUsCard',
  components: {},
  props: {
    icon: {
      type: String,
      required: false,
    },
    title: {
      type: String,
      required: true,
    },

    text: {
      type: String,
      required: true,
    },

    imgUrl: {
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
