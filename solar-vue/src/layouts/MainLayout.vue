<template>
  <q-layout view="lHh Lpr lff" class="bg-primary">
    <q-header elevated>
      <q-toolbar @click="router.push('/')">
        <!--
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />
        -->

        <q-toolbar-title style="no-margin">
             <q-img style="height:100%; max-width: 90px; margin:0;" src="../assets/pictures/logo/logo_SOLAR_no-bg.png"
             alt="Solar Kollektiv Logo" />
        </q-toolbar-title>

        <!-- <div>Quasar v{{ $q.version }}</div> -->
      </q-toolbar>
    </q-header>

    <!-- <q-drawer v-model="leftDrawerOpen" show-if-above bordered> -->
    <!--   <q-list> -->
    <!--     <q-item-label header> Essential Links </q-item-label> -->
    <!---->
    <!--     <EssentialLink -->
    <!--       v-for="link in essentialLinks" -->
    <!--       :key="link.title" -->
    <!--       v-bind="link" -->
    <!--     /> -->
    <!--   </q-list> -->
    <!-- </q-drawer> -->
    <!---->

    <q-page-container class="bg-primary">
      <router-view />
    </q-page-container>
    <FooterSimple/>
  </q-layout>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import EssentialLink from 'components/EssentialLink.vue';
import FooterSimple from 'components/FooterSimple.vue';
import {useRouter} from 'vue-router';


const linksList = [
  {
    title: 'Docs',
    caption: 'quasar.dev',
    icon: 'school',
    link: 'https://quasar.dev',
  },
  {
    title: 'Github',
    caption: 'github.com/quasarframework',
    icon: 'code',
    link: 'https://github.com/quasarframework',
  },
  {
    title: 'Discord Chat Channel',
    caption: 'chat.quasar.dev',
    icon: 'chat',
    link: 'https://chat.quasar.dev',
  },
  {
    title: 'Forum',
    caption: 'forum.quasar.dev',
    icon: 'record_voice_over',
    link: 'https://forum.quasar.dev',
  },
  {
    title: 'Twitter',
    caption: '@quasarframework',
    icon: 'rss_feed',
    link: 'https://twitter.quasar.dev',
  },
  {
    title: 'Facebook',
    caption: '@QuasarFramework',
    icon: 'public',
    link: 'https://facebook.quasar.dev',
  },
  {
    title: 'Quasar Awesome',
    caption: 'Community Quasar projects',
    icon: 'favorite',
    link: 'https://awesome.quasar.dev',
  },
];

export default defineComponent({
  name: 'MainLayout',

  components: {
    // EssentialLink,
    FooterSimple,
  },

  setup() {
    const leftDrawerOpen = ref(false);

    const router = useRouter();
    // const goToIndex = router.push('/');
    return {
      router,
     //goToIndex,
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>
