<template>
  <div>
    <v-data-table
        :headers="headers"
        :items="items"
        :items-per-page="2"
        class="elevation-1"
    >
      <template v-slot:no-data>
        <v-btn @click="furniture">
          Charger la météo
        </v-btn>
      </template>
    </v-data-table>
  </div>
</template>

<script>

export default {
  name: 'DataTable',
  props: ['furniture', 'headers', 'items']
}
</script>
