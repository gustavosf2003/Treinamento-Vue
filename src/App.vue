<template>
  <div id="app">


    <main class="container mt-3" >
      <h1>Usuários</h1>
      <hr>
      <div class="altura row mb-5 mt-3 ">

        <article class="col-sm-4 mt-3 " v-for="cliente in clientes" :key="cliente.id">
                                 
          <cliente :cliente="cliente"/>
          
        </article>
      
        


      </div>
    </main>
    <fim/>
  </div>
</template>



<script>

//? Importações dentro da pasta 'components'

import cliente from './components/cliente'
import fim from './components/fim'


//import produto from './components/produto'






export default {
  name: 'App',
  data(){
    return{
      
//TODO    Array com todos os dados do cliente

      clientes:[
        {
          id: 17,
        nome:"Maria",
        email:"maria@gmail.com",
        idade: 24,
        isPremium:false,
        },
          {
            id: 6,
          nome:"Gustavo",
          email:"gustavo@gmail.com",
          idade: 17,
          isPremium:true
          },
           {
             id: 3,
            nome:"Elon Musk",
            email:"elon@gmail.com",
            idade: 51,
            isPremium:false
            },
          {
            id: 45634,
          nome:"Bill Gates",
          email:"bill@gmail.com",
          idade: 68,
          isPremium:false
          },
          {
            id: 5435,
          nome:"Jack Dorsey",
          email:"47",
          idade: 17,
          isPremium:false
          },
          {
            id: 676,
          nome:"Steve Jobs",
          email:"steve@gmail.com",
          idade: 56,
          isPremium:true
          },
          {
            id: 678,
          nome:"Travis Kalanick",
          email:"travis@gmail.com",
          idade: 45,
          isPremium:true
          },
          {
            id: 98,
          nome:"Paul Mcartney",
          email:"paul@gmail.com",
          idade: 74,
          isPremium:false
          },{
          id: 235,
          nome:"Chris Martin",
          email:"Chris@gmail.com",
          idade: 38,
          isPremium:false
          }
         
          
      ]
    }
    
  },
  components: {
   cliente,
    fim,

  },

 

    }
</script>

<style>



.altura {
background-color:#F8F8F8;
  border-radius: 10px;
}



</style>




 

