<template>
  <div id="app">



  <div class="row mb-5 container mt-3 ">
    <input type="text" v-model="clienteGustavo.nome">
    <input type="text" v-model="clienteGustavo.email">
    <input type="number" v-model="clienteGustavo.idade">
    
    <cliente :cliente="clienteGustavo" :mostrarIdade="true"/>
    <cliente :cliente="clienteMaria" :mostrarIdade="false"/>
    
    <!-- <cliente nome="Warren Buffet" idade=85 email="gsferreira" descricao="adijdsljaskdjaskj"/> -->
    


  </div>

  </div>
</template>

<script>

//? Importações

import cliente from './components/cliente'
//import produto from './components/produto'






export default {
  name: 'App',
  data(){
    return{
      clienteGustavo:{
        nome:"Gustavo",
        email:"gsferreira2003",
        idade: 17
      },
      clienteMaria:{
        nome:"Maria",
        email:"",
        idade: 24
      }
    }
    
  },
  components: {
   cliente,

  }
}
</script>

<style>

</style>




 