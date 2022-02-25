<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="12" md="6">
      
      <v-card>
        <v-card-title class="headline">
          나만의 실전 포켓몬을 찾아서 검사를 시작해볼까요?
        </v-card-title>
        <v-img height="250" width="auto" src="img/titleimg.png" alt="포켓몬 그림" ></v-img>
        <v-card-text></v-card-text>
        
        <v-card-actions class="d-flex justify-center mb-6">
          
            <v-btn class="d-flex pa-2" width="200px" height="80px" color="primary" nuxt to="/inspire"> 고르기! </v-btn>
          
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>
<style>
  
  .btn{
    padding:10px;
  }
</style>