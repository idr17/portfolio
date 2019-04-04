<template>
  <q-layout view="lHh Lpr lFf">
    <!-- <q-layout-header>
      <q-toolbar
        color="red"
        :glossy="$q.theme === 'mat'"
        :inverted="$q.theme === 'ios'"
      >
        <q-btn
          flat
          dense
          round
          @click="leftDrawerOpen = !leftDrawerOpen"
          aria-label="Menu"
        >
          <q-icon name="menu" />
        </q-btn>

        <q-toolbar-title>
          Portfolio 1.0
          <div slot="subtitle">Running on Quasar v{{ $q.version }}</div>
          <div slot="subtitle">Sekelumit tentang</div>
        </q-toolbar-title>
      </q-toolbar>
    </q-layout-header> -->

    <q-layout-drawer
      v-model="leftDrawerOpen"
      :content-class="$q.theme === 'mat' ? 'bg-secondary' : null"
      :content-style="{color: '#fff'}"
      >
      <q-list
        no-border
        link
        inset-delimiter class="listMenu"
      >
        <q-item>
          <q-item-main style="text-align: center;">
            <q-item-tile style="display: block;"><img alt="Quasar logo" src="https://avatars1.githubusercontent.com/u/30069526?s=200&v=4" style="border-radius: 100px; height: 150px;"></q-item-tile>
            <q-item-tile style="display: block; font-weight: bold;">{{ creator.username }}</q-item-tile>
            <q-item-tile style="display: block;">{{ creator.progies }}</q-item-tile>
          </q-item-main>
        </q-item>
        <q-item />
        <q-item>
          <a name="about" href="#workingEksperience" class="links">
          <!-- <q-item-side icon="school" /> -->
          <q-item-main label="Jobs" sublabel="Experience" />
          </a>
        </q-item>
        <q-item>
          <a name="about" href="#portfolio" class="links">
          <!-- <q-item-side icon="school" /> -->
          <q-item-main label="Portfolio" sublabel="Projects" />
          </a>
        </q-item>
        <q-item>
          <a name="about" href="#about" class="links">
          <!-- <q-item-side icon="school" /> -->
          <q-item-main label="About" sublabel="Personal Information" />
          </a>
        </q-item>
      </q-list>
    </q-layout-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
    <q-layout-footer class="no-shadow">
      <q-toolbar color="secondary">
        <q-btn flat dense
          round @click="leftDrawerOpen = !leftDrawerOpen"
          aria-label="Menu"
        >
          <q-icon name="menu" />
        </q-btn>
        <q-toolbar-title>
          <p class="q-caption q-ma-none">By: {{ creator.nickname }}</p>
          <div slot="subtitle">call us @{{ creator.phone }} |
            <span @click="openURL(`https://github.com/${creator.github}`)" class="externalSrc">@github:{{ creator.github }}</span> |
            <span @click="openURL(`mailto:${creator.email}`)" class="externalSrc">@email:{{ creator.email }}</span></div>
        </q-toolbar-title>
      </q-toolbar>
    </q-layout-footer>
  </q-layout>
</template>

<script>
import { openURL } from 'quasar'

export default {
  name: 'MyLayout',
  data () {
    return {
      leftDrawerOpen: this.$q.platform.is.desktop,
      creator: {
        username: 'Indra Kurneamin',
        nickname: 'Indro',
        email: 'indera.allezz@gmail.com',
        github: 'idr17',
        phone: '081296171727',
        progies: 'Software Engineer'
      }
    }
  },
  methods: {
    openURL
  }
}
</script>

<style scoped>
.q-layout-page-container { font-family: 'Raleway', sans-serif; }
a.links { text-decoration: none; margin-left: 40px; color: #fff; }
.q-item-sublabel { color: #fff !important; }
span.externalSrc { cursor: pointer; }
</style>
