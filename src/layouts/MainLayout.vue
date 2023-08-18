<template>
  <q-layout view="lHh Lpr lFf">
    <q-header
      class="bg-white text-grey-10"
      bordered
    >
      <q-toolbar>
        <q-toolbar-title class="text-grand-hotel text-bold">
          Warsada App
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-footer
      class="bg-white small-screen-only"
      bordered
    >
      <q-toolbar class="text-grey-10 flex">
        <q-tabs
          v-model="tab"
          active-color="primary"
          indicator-color="transparent"
          class="full-width"
        >
          <q-route-tab
            to="/"
            name="home"
            icon="eva-home-outline"
            label="Home"
          />
          <q-route-tab
            to="/camera"
            name="camera"
            icon="eva-camera-outline"
            label="Camera"
          />
        </q-tabs>
      </q-toolbar>
    </q-footer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>

import {rule} from "postcss";

export default  {
  name: 'MainLayout',
  data () {
    return {
      tab: null
    }
  }
}
</script>

<style lang="sass">
.q-toolbar__title
  text-align: center
  font-size: 30px
.q-footer
  .q-tab__icon
    font-size: 50px
</style>
