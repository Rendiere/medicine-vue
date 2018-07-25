<template>
  <v-content>
    <section>
      <v-parallax src="https://cdn.vuetifyjs.com/images/parallax/material.jpg" height="600">
        <v-layout
          column
          align-center
          justify-center
          class="white--text">

          <img src="assets/logo.png" alt="logo" height="300">
          <h1 class="white--text mb-2 display-1 text-xs-center">Medicine</h1>
          <div class="subheading mb-3 text-xs-center">Monthly curated playlists</div>

        </v-layout>
      </v-parallax>
    </section>

    <section>
      <v-layout
        mt-5
        column
        wrap
        align-center
        justify-center>

        <!--Mixes heading-->
        <v-flex xs-12>
          <div class="text-xs-center">
            <h2 class="headline">Our Mixes</h2>
            <span class="subheading">A subheading...</span>
          </div>
        </v-flex>

        <!--Mixes list-->
        <v-flex xs-12>
          <v-container grid-list-xl>
            <v-layout row wrap align-center justify-center>
              <v-flex  xs12 s6 md4 v-for="mix in mixes" :key="mix.title">
                <v-card flat hover="true" ripple="true">
                  <v-card-title class="justify-center card--title">{{mix.title}}</v-card-title>
                  <v-card-media :src="mix.cover" height="200" width="200"></v-card-media>
                </v-card>
              </v-flex>
            </v-layout>

            <!--TODO: Load more when scrolled to bottom-->
          </v-container>
        </v-flex>
      </v-layout>

    </section>
  </v-content>

</template>

<script>
  export default {
    name: 'Home',
    data () {
      return {
        mixes: [
          {
            cover: '/static/images/FEB18.png',
            title: 'FEB18'
          },
          {
            cover: '/static/images/MAR18.png',
            title: 'MAR18'
          },
          {
            cover: '/static/images/APR18.png',
            title: 'APR18'
          },
          {
            cover: '/static/images/MAY18.png',
            title: 'MAY18'
          },
          {
            cover: '/static/images/JUNE18.png',
            title: 'JUN18'
          },
          {
            cover: '/static/images/JUL18.png',
            title: 'JUL18'
          },
          {
            cover: 'https://storage.googleapis.com/medicine-webpage/covers/DEC16_2.png',
            title: 'DEC16'
          }
        ]
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  .card--title {
    font-weight: lighter;
  }

  h1, h2 {
    font-weight: normal;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>
