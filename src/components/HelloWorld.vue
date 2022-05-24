<template>
 
    
<div class="card">
  <div class="card-body">
      <h1>{{titulo}}</h1>


    <form class="row g-3 needs-validation" novalidate>

      <div class="col-md-6">

        <label for="validationCustom01" class="form-label">Nome completo*</label>
        <input type="text" class="form-control" id="validationCustom01" placeholder="Digite o nome completo" value="" required>
        <div class="valid-feedback">
          Looks good!
        </div>

        <label for="validationCustom05" class="form-label">CPF*</label>
        <input type="text" class="form-control" id="validationCustom05" required>
        <div class="invalid-feedback">
         Please provide a valid zip.
        </div>

        <label for="validationCustom05" class="form-label">Número de celular*</label>
        <input type="text" class="form-control" id="validationCustom05" required>
        <div class="invalid-feedback">
          Please provide a valid zip.
        </div>
<div class="row">


<div class="col-md-3">
  <label for="validationCustom04" class="form-label">Estado*</label>
  <select class="form-select" id="validationCustom04" required>
    <option selected disabled value="">Choose...</option>
    <option>...</option>
  </select>
  <div class="invalid-feedback">
    Please select a valid state.
  </div>
    
  </div>
  <div class="col-md-3">
    <label for="validationCustom03" class="form-label">Cidade*</label>
    <input type="text" class="form-control" id="validationCustom03" required>
    <div class="invalid-feedback">
      Please provide a valid city.
    </div>
  </div>

</div>


<div class="my-3 col-md-3">
    <button class="btn btn-primary" type="submit">Proximo</button>
  </div>
      </div>
<div class="col-md-6">
  <img src="../assets/1.png" width="600em" alt="">

</div>

    </form>
  
  </div>
</div>

    

</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
   
  },
  data() {
    return {
      titulo: 'Sobre o professional'
    }
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1{
  font-weight: bold;
}
h3 {
  margin: 40px 0 0;
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
</style>
