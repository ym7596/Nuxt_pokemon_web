<template>
  <v-card
    class="mx-auto"
    
    height="100%">
    <v-img
    :src="monlist[randomNum].imgsrc"
    alt = "Image"
    height="auto"
    ></v-img>
    <v-card-title>
        <span>{{ monlist[randomNum].Name_ko }} ({{ monlist[randomNum].Name }})</span>
    </v-card-title>
    <v-card-subtitle>
        <span>{{ monlist[randomNum].Type1 }}</span>
        <span v-if="monlist[randomNum].Type2 != 'None'">/ {{ monlist[randomNum].Type2 }}</span>
    </v-card-subtitle>
    종족값 총합 : {{ monlist[randomNum].Total }}
    <v-row style="padding:12px;">
        <v-col><p style="font-size:11px">체력</p></v-col>
        <v-col><p style="font-size:11px">공격</p></v-col>
        <v-col><p style="font-size:11px">방어</p></v-col>
        <v-col><p style="font-size:11px">특공</p></v-col>
        <v-col><p style="font-size:11px">특방</p></v-col>
        <v-col><p style="font-size:9px">스피드</p></v-col>
      </v-row>
    <v-card-subtitle>
      
      <v-row>
        <v-col><span style="color:red;">{{ monlist[randomNum].H }}</span></v-col>
        <v-col><span style="color:rgb(92, 92, 253);">{{ monlist[randomNum].A }}</span></v-col>
        <v-col><span style="color:rgb(0, 255, 42);">{{ monlist[randomNum].B }}</span></v-col>
        <v-col><span style="color:rgb(204, 0, 160);">{{ monlist[randomNum].C }}</span></v-col>
        <v-col><span style="color:white;">{{ monlist[randomNum].D }}</span></v-col>
        <v-col><span style="color:yellow;">{{ monlist[randomNum].S }}</span></v-col>
      </v-row>
    </v-card-subtitle>
    <v-card-text>
      <span v-html ="monlist[randomNum].description"></span>
    </v-card-text>
    <v-card-text></v-card-text>
    <v-card-text></v-card-text>
    </v-card>
</template>

<script>

import monlist from '~/static/json/testdata.json'
export default {
    name:"InspirePage",
    asyncData({ params }) {
        return { monlist }
    },
    data() {
      return {
        randomNum : Math.ceil(Math.random()*100)}
      
    },
   
    
}

</script>
<style scoped>

</style>
