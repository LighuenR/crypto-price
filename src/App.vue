<template>
  <v-app>
    <v-app-bar>
      <h1>Crypto search</h1>
    </v-app-bar>
    <v-main>
      <v-container>
    <h1>Get Coin Data</h1>
    <v-text-field label="Coin name" v-model="coinName" @keydown.enter="$event =>getCoinData()"></v-text-field>
    <v-btn color="primary" @click="getCoinData()">Get Coin Data</v-btn>

    <v-card class="mt-12" v-if="coinData.id">
      <img :src="coinData.image.small" alt="">
      <v-card-title>{{ coinName.toUpperCase() }}:</v-card-title>

      <v-card-text>
        {{ coinData.description.en }}
      </v-card-text>
    </v-card>
  </v-container>
    </v-main>
  </v-app>
</template>

<script>

import axios from "axios";
export default {
  auth: false,
  data() {
    return {
      coinName: "",
      coinData: {},
    };
  },
  methods: {
    async getCoinData() {
      const response = await axios.get(
        `https://api.coingecko.com/api/v3/coins/${this.coinName}`
      );

      this.coinData = response.data;

      console.log(response.data);
    },
  },
};
</script>

<style>

</style>
