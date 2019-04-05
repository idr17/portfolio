<template>
  <q-layout view="lHh Lpr lFf">
    <q-layout-drawer v-model="leftDrawerOpen"
      :content-class="$q.theme === 'mat' ? 'bg-secondary' : null"
      :content-style="{color: '#fff'}" >
      <q-list no-border link inset-delimiter class="listMenu" >
        <q-item>
          <q-item-main class="circles">
            <q-item-tile class="item"><img alt="Quasar logo" src="https://avatars1.githubusercontent.com/u/30069526?s=200&v=4" style="border-radius: 100px; height: 150px;"></q-item-tile>
            <q-item-tile class="username">{{ creator.username }}</q-item-tile>
            <q-item-tile class="item">{{ creator.progies }}</q-item-tile>
          </q-item-main>
        </q-item>
        <q-item />
        <q-item>
          <a name="about" href="#workingEksperience" class="links">
          <q-item-main label="Jobs" sublabel="Experience" />
          </a>
        </q-item>
        <q-item>
          <a name="about" href="#portfolio" class="links">
          <q-item-main label="Portfolio" sublabel="Projects" />
          </a>
        </q-item>
        <q-item>
          <a name="about" href="#about" class="links">
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
        <q-btn flat dense round @click="leftDrawerOpen = !leftDrawerOpen" aria-label="Menu" >
          <q-icon name="menu" />
        </q-btn>
        <q-toolbar-title>
          <p class="q-caption q-ma-none">&copy; {{ creator.nickname }} {{ creator.copyright }}</p>
          <div slot="subtitle">call us @{{ creator.phone }} |
            <span @click="openURL(`mailto:${creator.email}`)" class="externalSrc">@email:{{ creator.email }}</span> |
            <span @click="openURL(`${creator.sourceCode}`)" class="externalSrc"> source code here!</span>
          </div>
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
        progies: 'Software Engineer',
        sourceCode: 'https://github.com/idr17/portfolio',
        copyright: '2019'
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
span.externalSrc { cursor: pointer; }
.circles { text-align: center; }
.circles .item { display: block; }
.circles .username { display: block; font-weight: bold; }
</style>
