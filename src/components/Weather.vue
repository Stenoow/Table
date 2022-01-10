<template>
  <div>
    <v-btn @click="getWeather">
      Charger la météo
    </v-btn>

    <v-data-table
        :headers="headers"
        :items="api"
        :items-per-page="2"
        class="elevation-1"
    ></v-data-table>
  </div>
</template>

<script>
const axios = require('axios').default;

export default {
  name: 'Weather',
  data () {

    return {
      headers: [
        { text: 'Jour', value: 'day_long' },
        { text: 'Date(J/M/A)', value: 'date' },
        { text: 'Temperature(C°) Max', value: 'tmax' },
        { text: 'Temperature(C°) Min', value: 'tmin' },
        { text: 'Conditions', value: 'condition' },
      ],
      api: [],
    }
  },
  methods: {
    getWeather(){
      var self = this;
      axios.get('https://www.prevision-meteo.ch/services/json/lat=46.259lng=5.235').then(function(response){
        self.api = [];
        for(let i = 0; i<5; i++){
          self.api.push( response.data['fcst_day_' + i]);
        }

      });
    }
  }
}
</script>
