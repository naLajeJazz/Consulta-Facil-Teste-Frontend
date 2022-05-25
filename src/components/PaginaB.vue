<template>
 
 <div class="container">

 
    
      <div class="card mx-5 mb-5 p-3 shadow rd text-start">
          <div class="card-body ">
            <h1 class="mb-3 text-start">{{titulo}}</h1>
            <h3 class="my-5 text-start">Detalhes do atendimento</h3>


            <form  class="row g-3 needs-validation ">
              <div class="col-md-6 ">
                <label for="validationCustom01" class="form-label my-3">Especialidade principal*</label>
                  
                  <select class="form-select" aria-label="Default select example"  >
                    <option selected >Selecione a especialidade</option>
                    <option value="1">One</option>
                    <option value="2">Two</option>
                    <option value="3">Three</option>
                  </select>
        
                <label for="validationCustom05" class="form-label my-3">Informe o valor*</label>
                <div class="col-md-9">
                  
                  <div class="input-group mb-3 ">
                    <span class="input-group-text bck text-light">R$</span>
                    <input type="text" class="form-control" aria-label="Dollar amount (with dot and two decimal places)" required>
                  </div>
                </div>
        
        <label for="validationCustom05" class="form-label my-3">Formas de pagamento da consulta*</label>
        <div class="card shadow-sm my-3">
          <div class="card-body bck2">
            <div class="form-check">
              <input class="form-check-input " type="checkbox" name="flexRadioDefault" id="flexRadioDefault1">
                <label class="form-check-label " for="flexRadioDefault1">
                Em dinheiro
                </label>
            </div>
          </div>
        </div>

        <div class="card shadow-sm">
          <div class="card-body bck2">
            <div class="form-check ">
              <input class="form-check-input" type="checkbox" name="flexRadioDefault" id="flexRadioDefault1">
                <label class="form-check-label" for="flexRadioDefault1">
                Pix
                </label>
            </div>
          </div>
        </div>

        <div class="card shadow-sm my-3">
          <div class="card-body bck2">
            <div class="form-check ">
              <input class="form-check-input" type="checkbox" name="flexRadioDefault" id="flexRadioDefault1">
                <label class="form-check-label" for="flexRadioDefault1">
                Cartão de crédito
                </label>
            </div>
          </div>
        </div>

       
     
       

<div class="row justify-content-center my-5 ">
  <div class="bar col-md-6"></div>
  
  <div class="col-md-3">
    <span class="">2 de 2</span>

  </div>

</div>

<div class="my-3 col-md-12 d-grid gap-2 bck rd " >
    <button  class="btn text-light" type="submit">PRÓXIMO</button>
  </div>

      </div>
<div class="col-md-6 my-5 ">
  <img src="../assets/2.png" width="90%" alt="">

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
      titulo: 'Sobre o Atendimento'
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
  font-family: 'Open Sans', sans-serif;
  color: #282828;
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
