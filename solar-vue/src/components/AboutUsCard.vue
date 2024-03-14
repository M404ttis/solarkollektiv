<template>
  <div id="about-us-card">
    <!-- <q-card class="row justify-center q-ma-md q-pa-sm">
      <q-img :src=$props.srcPath fit="cover"  :img-style="{ opacity: '0.3' }"  class="">
        <div class="q-mb-md absolute-top text-center">{{ title }}</div>
        <p class="q-ma-xs absolute-bottom overflow-auto">
          {{ text }}
        </p>
      </q-img>
    </q-card> -->

    <q-card class="my-card q-ma-md q-pa-sm">
      <q-img :src="$props.srcPath" rounded-borders>
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
    srcPath: {
      type: String,
      required: false,
    },
  },
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped></style>
