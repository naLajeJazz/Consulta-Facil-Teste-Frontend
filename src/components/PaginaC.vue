<template>
 
    <div class="container">

          <div class="card mx-5 mb-5 p-3 shadow rd">
            <div class="card-body row">
              
              <h1 class="mb-3 text-start">{{titulo}}</h1>

                  <div class=" col-md-6">

                    <ul class="my-4 list text-start">
                      <li class="mb-4 list-group-item" v-for="cadastro in lista" :key="cadastro.id" >
                      {{cadastro}}
                      
                      </li>
                      
                    </ul>

                    
                    
                   
                    <div class="my-4 col-md-12 d-grid  bck rd " >
                      <button  class="btn text-dark fw-bold" type="submit">CADASTRAR PROFISSIONAL</button>
                    </div>

                    <div>
                     <a href="" class="fw-bold">Editar cadastro</a> 
                    </div>

                  </div>


            
                  <div class=" col-md-6   ">

                    <img src="../assets/3.png"   alt="imagem">

                  </div>
            
            </div>

          </div>

    </div> 

</template>

<script>
export default {
  name: 'PaginaB',
  props: {
    msg: String
   
  },
  data() {
    return {
      titulo: 'Revisão do cadastro',
      lista: ['Nome completo','CPF','Número de celular ou telefone','Estado/Cidade',
      'Especialidade principal','Preço da consulta','Formas de pagamento da consulta'],
    }
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1{
  font-family: 'Comfortaa', cursive, Helvetica, Arial, sans-serif;
  font-weight: bold;
 
}
h3 {
  font-family: 'Open Sans', sans-serif;
  font-weight:lighter;
  color: #282828;
 
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  font-family: 'Open Sans', sans-serif;
  font-weight:bold;
  color: #282828;
}
a {
  text-decoration: none;
  color: #483698;
}
img {
  width:90%;
}
</style>

<style scoped>
.rd{
  border-radius: 16px;
}
.bck{
  background-color: #FBDE40;
}
.bar{
  background-color: #483698;
  width: 70%;
  height: 25px;
  border-radius:2px;
}
.bar2{
  background-color: #B9B9B9;
  width: 35%;
  height: 25px;
  border-radius:2px;
}
.bck2 {
  background-color: #F9F9F9;
}
.borda{
  border: 1px solid red;
}
</style>
