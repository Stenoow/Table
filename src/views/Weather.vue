<template>
  <div class="home">
    <Layout />
    <DataTable v-bind:furniture="getWeather" v-bind:headers="headers" v-bind:items="items"/>
  </div>
</template>

<script>
import DataTable from '@/components/DataTable.vue';
import Layout from '@/components/Layout.vue';
import {default as axios} from "axios";

export default {

  name: 'Weather',
  components: {
    DataTable,
    Layout
  },
  data () {

    return {
      headers: [
        { text: 'Jour', value: 'day_long' },
        { text: 'Date(J/M/A)', value: 'date' },
        { text: 'Temperature(C°) Max', value: 'tmax' },
        { text: 'Temperature(C°) Min', value: 'tmin' },
        { text: 'Conditions', value: 'condition' },
      ],
      items: []
    }
  },
  methods: {
    getWeather(){
      const self = this;
      axios.get('https://www.prevision-meteo.ch/services/json/lat=46.259lng=5.235').then(function(response){
        self.items = [];

        for(let i = 0; i<5; i++){
          self.items.push( response.data['fcst_day_' + i]);
        }
        console.log(self.items)
      });
    }
  }
}
</script>
