<template>
<div id="contenedor" class="container">
        <div class="row">
            <div class="col s12">
                <h3>Lista de cosas random de <span>{{usuario}}</span></h3>
            </div>
        </div>
        <div class="row">
            <div class="col s12">
                <h5 v-if="encabezado1 == true">Miembros de la familia Simpson</h5>
                <ul class="collection">
                    <li class="collection-item" v-for="(miembro,i) in miembros" v-bind:key="i">{{miembro}}</li>
                </ul>
            </div>
        </div>
    </div>  
</template>


<script>
export default {
  
  name: 'MiLista',
  data:function() {
    return{
      miembros: ['Bart','Lisa','Homero','Marge','Maggie'],
      encabezado1 : true,
      usuario: "Pablo",
      }     
  }

}
</script>

<style scoped>

#contenedor{
  background-color: #42b883;

}

span{
  color: #35495e
}

h3, h5{
  color: white;
}




</style>