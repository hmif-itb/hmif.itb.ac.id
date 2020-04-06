<template>
  <client-only>
    <div>
      <v-app-bar
        color="transparent"
        elevation="0"
      >
        <v-container class="py-0 px-0" align="center" fill-height>
          <v-layout>
            <v-toolbar-title>
              <v-container fill-height class="pa-0">
                <nuxt-link to="/">
                  <v-img :src="require('~/assets/img/logo-hmif.png')" width="35" style="margin-right: 15px" />
                </nuxt-link>
              </v-container>
            </v-toolbar-title>

            <v-icon small color="#FFC107" class="mr-1">fas fa-chevron-right</v-icon>

            <v-toolbar-items v-bind:class="{'should-hide': $vuetify.breakpoint.smAndDown}">
              <template v-for="(menu, i) in menus">
                <v-btn :key="i" v-if="!menu.external" class="text-capitalize spacing-normal" text :to="menu.to" :exact="menu.exact">
                  {{ menu.title }}
                </v-btn>
                <v-btn :key="i" v-else class="text-capitalize spacing-normal" text :href="menu.to">
                  {{ menu.title }}
                  <v-icon small class="ml-2" style="font-size: 8pt">fas fa-external-link-alt</v-icon>
                </v-btn>
              </template>
            </v-toolbar-items>
            <v-spacer />
            <v-toolbar-items class="hidden-md-and-up">
              <v-btn icon @click="drawer = !drawer">
                <v-icon small>fas fa-bars</v-icon>
              </v-btn>
            </v-toolbar-items>
          </v-layout>
        </v-container>
      </v-app-bar>
      <v-navigation-drawer v-model="drawer" app disable-resize-watcher>
        <v-list>
          <template v-for="(menu, i) in menus">
            <v-list-item :key="i" v-if="!menu.external" :to="menu.to" :exact="menu.exact">
              <v-list-item-title>{{ menu.title }}</v-list-item-title>
            </v-list-item>
            <v-list-item :key="i" v-else :href="menu.to">
              <v-list-item-title>
                {{ menu.title }}
                <v-icon small class="ml-2" style="font-size: 8pt">fas fa-external-link-alt</v-icon>
              </v-list-item-title>
            </v-list-item>
          </template>
        </v-list>
      </v-navigation-drawer>
    </div>
  </client-only>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      drawer: false,
      menus: [
        { title: "Home", to: "/", exact: true },
        { title: "About", to: "/about" },
        { title: "Contact", to: "/contact" },
        { title: "Inkubator-IT", to: "https://inkubatorit.com", external: true },
      ]
    }
  }
}
</script>

<style scoped>
  .spacing-normal {
    letter-spacing: normal;
  }

  .v-btn--active {
    font-weight: bold;
  }

  .v-btn--active:before {
    background: none;
  }

  .should-hide .v-btn:not(.v-btn--active) {
    display: none;
  }
</style>
