<template>
  <v-container fluid fill-height>
    <v-row>
      <v-col cols="12" xl="12" class="text-center">
        <h1 id="marx" class="text-h2">MARX IPSUM</h1>
      </v-col>
      <v-col cols="12" class="text-center">
         <v-avatar size="200">
          <img
            src="https://upload.wikimedia.org/wikipedia/commons/f/fc/Karl_Marx.jpg"
            alt="Marx"
          >
        </v-avatar>
      </v-col>
      <v-col cols="12" class="text-center">
        <v-text-field
          label="Outlined"
          outlined
          clearable
          v-model="cantiWords"
        >
        </v-text-field>
      </v-col>
      <v-col cols="12" class="text-center">
        <v-btn v-on:click="generateWords">Generar palabras</v-btn>
      </v-col>
      <v-col cols="12" class="text-center">
        <p>{{ frase }}</p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: function () {
    return {
      words: ['communism', 'marxist', 'accidental', 'and', 'purely', 'let', 'us', 'values', 'manifests', 'capital', 'buy', 'capitalist', 'farmer', 'is', 'not', 'very', 'then', 'the', 'bad', 'people', 'proletary', 'taxes', 'money', 'kind', 'production', 'Kapital', 'society?', 'modern', 'economy', 'system?', 'illusion', 'commodity', 'superstition', 'our', 'we', 'comrade', 'value', 'system', 'how', 'those', 'main', 'Engel', 'exchange', 'valuable', 'Berlin', 'element', 'by-the-buy', 'little', 'truth', 'poor', 'poorless', 'Nature', 'creations', 'economists', 'gold', 'silver', 'response', 'represion', 'state', '.'],
      cantiWords: 1,
      frase: []
    }
  },

  methods: {
    generateWords () {
      var cant = this.cantiWords
      console.log(cant)
      this.frase = []
      for (var i = 0; i < cant; i++) {
        var number = Math.floor(Math.random() * this.words.length)
        var phrase = this.words[number]
        // eslint-disable-next-line no-unused-expressions
        this.frase.push(phrase)
      }
    }
  }
}
</script>

<style>

</style>
