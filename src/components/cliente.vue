<template>

 <div class="col-sm-4 mt-3 ">
        <div class="card h-100 ">
            <div class="card-body ">
                <h4 class="card-title font-weight-bold text-monospace ">{{cliente.nome}}</h4>
                <hr>
                <div class="ml-1">
                    <p class="card-text mt-3"><span class="font-weight-bold text-monospace ">Descrição: </span>{{cliente.descricao}}
                    <p class="card-text"><span class="font-weight-bold text-monospace">Email: 
                        </span>{{cliente.email}}
                    </p>
                    <p class="card-text" v-if="cliente.idade >=18">
                        
                        Idade:{{cliente.idade}}
                    </p>
                    <p class="card-text" v-else>Menor de idade</p>

                    <p class="card-text" v-show="cliente.email.length != 0" >
                        
                        Este usuário possui email
                    </p>
                   

                    

                    
                    

                </div>


                <div class="row mt-2" >
                    <div class="">
                        
                            <button type="button" class="btn btn-outline-warning btn-sm  ">
                                Editar 
                            </button>
                        
                    </div>
                </div>

            </div>
        </div>
    </div>

 
</template>

<script>


export default {



    
    props:{
        
        cliente:Object,
        mostrarIdade:Boolean,
        
    }

}




</script>

<style scoped>








</style>

