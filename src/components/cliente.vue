//! Este componente adiciona o card de cada usuário, que as informações estão dentro do array "clientes" no App.js. 
//! O array foi percorrido através do laço de repetição v-for e tem o nome "fim"


<template>

<!-- Card de usuário -->
        <section class="card h-100 ">
            <div class=" card-body">
                <div >

                    <!-- Classe será alterada para 'isPremium' caso o usuário possua assinatura Premium -->

                    <h4 class="card-title font-weight-bold text-monospace " :class="{'cliente': !cliente.isPremium,'isPremium':cliente.isPremium}">{{cliente.nome}}</h4>
                    <hr>
                    <div class="ml-1">
                        <p class="card-text mt-3"><span class="font-weight-bold text-monospace ">Descrição: </span>{{cliente.id}}


                        <!-- Treinando o V-show -->
                        <p class="card-text" v-show="cliente.email.length != 0">
                            Email: {{cliente.email}}
                        </p>

                         <p class="card-text" style="color:red"  v-show="cliente.email.length == 0" >
                            
                           <u> *Este usuário não possui email </u>
                        </p>

                        

                        <!-- Treinando V-If -->

                        <p class="card-text" v-if="cliente.idade >=18">
                            
                            Idade:{{cliente.idade}}
                        </p>
                        <p class="card-text" v-else>Menor de idade</p>


                        <p class="card-text" v-if="cliente.isPremium">
                            
                            Este cliente é <u style="color:goldenrod">Premium </u>
                        </p>
                        <p class="card-text" v-else>Este cliente não é Premium</p>



                    </div>


                    <section class="row mt-2" >
                        
                            
                                <button type="button" class="btn btn-outline-warning btn-sm ml-3"  @click="abrirAlert">
                                    Editar 
                                </button>
                            
                        
                    </section>
                </div>
            </div>
        </section>
  

 
</template>

<script>



export default {


data(){
    return{
    isPremium:false
    }
},
    
    props:{
        
        cliente:Object,
        mostrarIdade:Boolean,
        
        
    },
    methods:{
        abrirAlert: function(){
            alert("Este alert foi aberto com a propriedade methods do Vue methods, \nquerido usuário: " + this.cliente.nome)
        }
    }

}




</script>

<style scoped>

.isPremium{
    
    color: goldenrod;
}




</style>

