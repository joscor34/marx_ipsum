<template>
  <v-app>
    <v-main>
      <Main/>
    </v-main>
    <v-footer padless color="black">
      <v-col
        class="text-center"
        cols="12"
        v-on:click="goTwitter"
      >
       <p class="text-h6" id="footer">Made by @HoraIntelectual ❤️</p>
      </v-col>
    </v-footer>
  </v-app>
</template>

<script>
import Main from './components/Main'

export default {
  name: 'App',

  components: {
    Main
  },

  data: () => ({
    //
  }),

  methods: {
    goTwitter: () => {
      window.open('https://twitter.com/HoraIntelectual', '_blank')
    }
  }
}
</script>

<style>
#footer{
  color: white;
}
</style>
