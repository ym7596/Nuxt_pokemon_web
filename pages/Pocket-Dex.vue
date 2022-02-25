<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      
      <v-card>
        <v-card-title class="headline">
          실전 도감
        </v-card-title>
        <v-row>
            <v-col v-for="(data,index) in monlist" :key="index" cols="6">
              <PCard :data = "data" />
            </v-col>
        </v-row>
        
      </v-card>
    </v-col>
  </v-row>
</template>
<script>
import monlist from '~/static/json/testdata.json'
export default {
    name:"PocketDex",
    asyncData({ params }) {
        return { monlist }
    },
}
</script>
<style>
    
</style>