<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="bg-white">
      <q-toolbar>
        <q-btn flat dense round @click="leftDrawerOpen = !leftDrawerOpen" aria-label="Menu">
          <q-icon class="text-red" name="menu" />
        </q-btn>

        <q-toolbar-title class="text-red">Pet Santana</q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered content-class="bg-deep-pink-2">
      <q-parallax class="full-height" src="https://wallpaperplay.com/walls/full/0/8/a/72458.jpg">
        <q-list>
          <q-item clickable tag="a" href="http://localhost:8080/#/">
            <q-item-section avatar>
              <q-icon name="fa fa-dog" />
            </q-item-section>
            <q-item-section>
              <q-item-label>Pagina inicial</q-item-label>
            </q-item-section>
          </q-item>
          <q-item clickable tag="a" href="http://localhost:8080/#/cadCliente">
            <q-item-section avatar>
              <q-icon name="fa fa-user" />
            </q-item-section>
            <q-item-section>
              <q-item-label>Cadastrar Clientes</q-item-label>
            </q-item-section>
          </q-item>
          <q-item clickable tag="a" href="http://localhost:8080/#/cadPet">
            <q-item-section avatar>
              <q-icon name="fa fa-paw" />
            </q-item-section>
            <q-item-section>
              <q-item-label>Cadastrar Pets</q-item-label>
            </q-item-section>
          </q-item>
        </q-list>
      </q-parallax>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { openURL } from 'quasar'

export default {
  name: 'MyLayout',
  data () {
    return {
      leftDrawerOpen: false
    }
  },
  methods: {
    openURL
  }
}
</script>
