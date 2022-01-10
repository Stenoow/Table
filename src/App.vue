<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >

      <v-toolbar-title>Weather | La météo de Demain !</v-toolbar-title>

    </v-app-bar>

    <v-main>
      <Weather/>
    </v-main>
  </v-app>
</template>

<script>
import Weather from './components/Weather.vue';

export default {
  name: 'App',

  components: {
    Weather,
  },

  data: () => ({
    //
  }),
};
</script>
