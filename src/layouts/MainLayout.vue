<template>
  <q-layout view="lHh Lpr lFf">
    <!--<q-header elevated> == shadow-->
    <q-header>
      <!--Toolbar-->
      <!-- <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />

        Title and version
        <q-toolbar-title>
          Quasar App
        </q-toolbar-title>
        <div>Quasar v{{ $q.version }}</div>

        <div>
          <div class="-text-h3"></div>
        </div>

      </q-toolbar> -->
    </q-header>

    <!--Lateral menu-->
    <!-- <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-1"
    >
      <q-list>
        <q-item-label
          header
          class="text-grey-8"
        >
          Essential Links
        </q-item-label>
        
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer> -->

    <!--Logo/home page-->
    <!-- <q-page-container>
      <router-view />
    </q-page-container> -->

    <div class="window-height window-width row justify-center items-center">
      <div class="q-pa-md q-gutter-sm">
        <q-btn color="primary" label="Primary" size="500%" />
        <q-btn color="secondary" label="Secondary" size="500%" />
      </div>
    </div>

    <div class="window-height window-width row justify-center items-center">
      <div class="q-pa-md q-gutter-sm">
        <q-btn color="primary" label="Tertiary" size="500%" />
        <q-btn color="secondary" label="Quaternary" size="500%" />
      </div>
    </div>
  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink.vue'

const linksData = [
  {
    title: 'Docs',
    caption: 'quasar.dev',
    icon: 'school',
    link: 'https://quasar.dev'
  },
  {
    title: 'Github',
    caption: 'github.com/quasarframework',
    icon: 'code',
    link: 'https://github.com/quasarframework'
  },
  {
    title: 'Discord Chat Channel',
    caption: 'chat.quasar.dev',
    icon: 'chat',
    link: 'https://chat.quasar.dev'
  },
  {
    title: 'Forum',
    caption: 'forum.quasar.dev',
    icon: 'record_voice_over',
    link: 'https://forum.quasar.dev'
  },
  {
    title: 'Twitter',
    caption: '@quasarframework',
    icon: 'rss_feed',
    link: 'https://twitter.quasar.dev'
  },
  {
    title: 'Facebook',
    caption: '@QuasarFramework',
    icon: 'public',
    link: 'https://facebook.quasar.dev'
  },
  {
    title: 'Quasar Awesome',
    caption: 'Community Quasar projects',
    icon: 'favorite',
    link: 'https://awesome.quasar.dev'
  }
];

export default {
  name: 'MainLayout',
  components: { EssentialLink },
  data () {
    return {
      leftDrawerOpen: false,
      essentialLinks: linksData
    }
  }
}
</script>

<style lang="scss">
  .divButton {
    // text-align: center;
    // vertical-align: center;
    // margin: auto;
    // margin-left: auto;
    // margin-right: auto;
    position: absolute;

  }
</style>