<template>
  <q-layout view="hHh lpR fFf">
    <q-header elevated class="navbar layout">
      <div class="logoContainer">
        <q-img class="logo" src="/logo.png" />
      </div>
      <q-tabs class="navtabs" align="right">
        <q-route-tab to="/" label="Home" />
        <q-route-tab to="/AboutMe" label="About Me" />
        <q-route-tab to="/Projects" label="My Projects" />
      </q-tabs>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import EssentialLink, {
  EssentialLinkProps,
} from 'components/EssentialLink.vue';

const essentialLinks: EssentialLinkProps[] = [
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

const leftDrawerOpen = ref(false);

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value;
}
</script>

<style lang="scss">
.logoContainer {
  display: flex;
  flex-direction: column;
  align-items: center; /* Centering x-axis */
}

.navtabs {
  margin-top: $default-margin;
  margin-right: $default-margin;
  color: black;
}

.navtabs .q-tab__label {
  font-family: american-captain;
  margin: 0 2rem;
  padding: 0 $default-padding;
  font-size: 1.5rem;
}
.layout {
  padding-top: $default-padding;
}
.navbar {
  background-color: transparent;
}
.logo {
  width: 31.25rem;
  margin: auto;
}
</style>
