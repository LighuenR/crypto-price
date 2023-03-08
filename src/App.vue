<template>
  <v-app>
    <v-app-bar>
      <h1>Crypto search</h1>
    </v-app-bar>
    <v-main>
      <v-container>
        <v-card class="mx-auto" max-width="400">
          <v-text-field label="Ingrese nombre de cryptomoneda" >
          </v-text-field>
          <v-btn>
            Enviar
          </v-btn>
        </v-card>
      </v-container>

      <v-container>
        <v-card class="mx-auto" max-width="400" prepend-icon="mdi-home">
          <template v-slot:title>
            This is a title
          </template>
          <v-card-text>
            This is content
          </v-card-text>
        </v-card>
      </v-container>


    </v-main>
  </v-app>
</template>

<script>


export default {
  name: 'App',

  components: {

  },

  data: () => ({
    //
  }),
}
</script>

<style>
. {
  padding: 0;
  margin: ;
}
</style>
