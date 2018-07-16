<template>
  <v-app light>

    <v-navigation-drawer v-model="sideNav" fixed>
      <v-list>
        <v-list-tile>
          <v-list-tile-action>
            <v-icon>music_note</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>Mixes</v-list-tile-content>
        </v-list-tile>

        <v-list-tile>
          <v-list-tile-action>
            <v-icon>group_add</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>Sign Up</v-list-tile-content>
        </v-list-tile>

        <v-list-tile>
          <v-list-tile-action>
            <v-icon>graphic_eq</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>About</v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>

    <v-toolbar flat @click.stop="sideNav = false">
      <v-toolbar-side-icon
        class="hidden-sm-and-up"
        @click.stop="sideNav = !sideNav">
      </v-toolbar-side-icon>


      <v-toolbar-title>Medicine Monthly</v-toolbar-title>

      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-xs-only">
        <v-btn flat>
          <v-icon left>music_note</v-icon>
          Mixes
        </v-btn>

        <v-btn flat>
          <v-icon left>group_add</v-icon>
          Sign Up
        </v-btn>

        <v-btn flat>
          <v-icon left>graphic_eq</v-icon>
          About
        </v-btn>
      </v-toolbar-items>
    </v-toolbar>

    <main>
      <router-view></router-view>
    </main>

  </v-app>
</template>

<script>
  export default {
    data () {
      return {
        sideNav: false
      }
    },
    name: 'App'
  }
</script>
