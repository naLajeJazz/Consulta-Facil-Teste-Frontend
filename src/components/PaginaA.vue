<template>
 
 <div class="container">

 
    
<div class="card mx-5 mb-5 p-3 shadow rd">
  <div class="card-body ">
      <h1 class="mb-3 text-start">{{titulo}}</h1>
      <h3 class="my-5 text-start">Dados do profissional</h3>


    <form  class="row g-3 needs-validation "   >

      <div class="col-md-6 text-start">

        <label for="validationCustom01" class="form-label my-3 ">Nome completo*</label>
        <input type="text" class="form-control" id="validationCustom01" placeholder="Digite o nome completo" value="" required>
        <div class="valid-feedback">
          Looks good!
        </div>

        <label for="validationCustom05" class="form-label my-3" aria-placeholder="ola">CPF*</label>
        <input type="text" class="form-control" id="validationCustom05" required>
        <div class="invalid-feedback">
         Please provide a valid zip.
        </div>

        <label for="validationCustom05" class="form-label my-3">Número de celular*</label>
        <input type="text" class="form-control" id="validationCustom05" required>
        <div class="invalid-feedback">
          Please provide a valid zip.
        </div>
<div class="row">


<div class="col-md-6">
  <label for="validationCustom04" class="form-label my-3">Estado*</label>
  <select class="form-select" id="validationCustom04" required>
    <option selected disabled value="">selecione o estado</option>
    <option v-for="est in estado" :key="est.id">{{est.nome}}</option>
  </select>
  
    
  </div>
  <div class="col-md-6">
    <label for="validationCustom03" class="form-label my-3">Cidade*</label>
    <select class="form-select" id="validationCustom04" required>
    <option selected disabled value="">selecione a cidade</option>
    <option v-for="cid in cidade" :key="cid.id">{{cid.nome}}</option>
  </select>
  </div>

</div>
<div class="row justify-content-center my-5 ">
  <div class="bar col-md-3"></div>
  <div class="bar2 col-md-3"></div>
  <div class="col-md-3">
    <span class="">1 de 2</span>

  </div>

</div>

<div class="my-3 col-md-12 d-grid gap-2 bck rd " >
    <button  class="btn text-light" type="submit">PRÓXIMO</button>
  </div>

  <div v-for="c in cpf" :key="c.id">{{c.cpf}}</div>

      </div>
<div class="col-md-6 my-5 ">
  <img src="../assets/1.png"  alt="">

</div>

    </form>
  
  </div>
</div>

   </div> 

</template>

<script>
import axios from 'axios'
export default {
  name: 'PaginaA',
  props: {
    msg: String
   
  },
  data() {
    return {
      titulo: 'Sobre o professional',
      estado: [],
      cidade: [],
      cpf: []
      
    }
  },
  mounted () {
    axios
      .get('https://api-teste-front-end-fc.herokuapp.com/estados')
      .then(response => (this.estado = response.data))
    axios
      .get('https://api-teste-front-end-fc.herokuapp.com/cidades')
      .then(response => (this.cidade = response.data))
    axios
      .get('https://api-teste-front-end-fc.herokuapp.com/profissionais')
      .then(response => (this.cpf = response.data))
  }

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
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
label{
  font-family: 'Open Sans', sans-serif;
  color: #282828;
}
img {
  width: 90%;
}
</style>

<style scoped>
.rd{
  border-radius: 16px;
}
.bck{
  background-color: #483698;
}
.bar{
  background-color: #483698;
  width: 35%;
  height: 25px;
  border-radius:2px;
}
.bar2{
  background-color: #B9B9B9;
  width: 35%;
  height: 25px;
  border-radius:2px;
}
.borda{
  border: 1px solid red;
}
</style>
