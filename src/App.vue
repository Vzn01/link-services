<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import item from "./components/item.vue"
</script>

<script>
import Dados from "./Dados/services.json"
  export default{
    data(){ 
      return{
      servicos: null
      }
    },
    mounted(){
      this.servicos = Dados;
      //console.log(Dados)
    }
    
  }
</script>

<template>
  <img src="./assets/vue.svg" style="width:100px" class="logo vue" alt="Vue logo" />
  <h1>Seja Bem vindo(a)</h1>
  <hr/>
  <div class="itens">
    <item
    v-for="servico, index in servicos"
    :key="index"
    :item="servico"
    />
  </div>
</template>

<style>
  .itens{
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
  }

  html{
    background: url("https://images.alphacoders.com/121/1218911.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    min-height: 110%;
  }
</style>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}


</style>
