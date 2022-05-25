<template>
 
 <div class="container">

 
    
<div class="card mx-5 mb-5 p-3 shadow rd">
  <div class="card-body ">
      <h1 class="mb-3">{{titulo}}</h1>
      <h3 class="mb-3 text-start">Dados do profissional</h3>


    <form  class="row g-3 needs-validation "   >

      <div class="col-md-6 ">

        <label for="validationCustom01" class="form-label my-3">Nome completo*</label>
        <input type="text" class="form-control" id="validationCustom01" placeholder="Digite o nome completo" value="" required>
        <div class="valid-feedback">
          Looks good!
        </div>

        <label for="validationCustom05" class="form-label my-3">CPF*</label>
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
    <option selected disabled value="">Choose...</option>
    <option>...</option>
  </select>
  <div class="invalid-feedback">
    Please select a valid state.
  </div>
    
  </div>
  <div class="col-md-3">
    <label for="validationCustom03" class="form-label my-3">Cidade*</label>
    <input type="text" class="form-control" id="validationCustom03" required>
    <div class="invalid-feedback">
      Please provide a valid city.
    </div>
  </div>

</div>


<div class="my-3 col-md-6">
    <button  class="btn btn-primary" type="submit">Proximo</button>
  </div>
      </div>
<div class="col-md-6 my-5">
  <img src="../assets/1.png" width="90%" alt="">

</div>

    </form>
  
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
      titulo: 'Sobre o professional2'
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
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
label{
  color: #282828;
}
</style>

<style>
.rd{
  border-radius: 25px;
}
</style>
