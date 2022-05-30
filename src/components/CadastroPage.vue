<template>

  <a  href="#" @click="v()">  
<div class="text-start text-dark fw-bold container ms-5 p-3" >
<svg  xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" class="bi bi-chevron-left" viewBox="0 0 16 16">
  <path fill-rule="evenodd" d="M11.354 1.646a.5.5 0 0 1 0 .708L5.707 8l5.647 5.646a.5.5 0 0 1-.708.708l-6-6a.5.5 0 0 1 0-.708l6-6a.5.5 0 0 1 .708 0z"/>
</svg>
  </div>
</a>
<div class="container">
    <div class="card mx-5 mb-5 p-3 shadow rd">
      <div class="card-body ">
        <div>{{seletorPage}}</div>
        <div class="paginaA" v-if="seletorPage==0">
        <h1 class="mb-3 text-start">Sobre o professional</h1>
        <h3 class="my-5 text-start">Dados do profissional</h3>

      <form  class="row g-3 needs-validation "   >

      <div class="col-md-6 text-start">

        <label for="validationCustom01" class="form-label my-3 ">Nome completo*</label>
        <input type="text" class="form-control"  placeholder="Digite o nome completo"  v-model="nomeData" required>
       

        <label for="validationCustom05" class="form-label my-3" aria-placeholder="ola">CPF*</label>
        <input type="text" class="form-control" v-model="cpfData" required>
        <div class="invalid-feedback">
         Please provide a valid zip.
        </div>

        <label for="validationCustom05" class="form-label my-3">Número de celular*</label>
        <input type="text" class="form-control" v-model="telefoneData" required>
        
<div class="row">


<div class="col-md-6">
  <label for="validationCustom04" class="form-label my-3">Estado*</label>
  <select class="form-select" id="validationCustom04" v-model="estadoData" required>
    <option selected disabled value="">selecione o estado</option>
    <option v-for="est in estado" :key="est.id">{{est.nome}}  </option>
  </select>
  
    
  </div>
  <div class="col-md-6">
    <label for="validationCustom03" class="form-label my-3">Cidade*</label>
    <select class="form-select" id="validationCustom04" v-model="cidadeData" required>
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


<!--     

  <div v-for="c in cpf" :key="c.id">{{c.cpf}}</div>
-->

      </div>
<div class="col-md-6 my-auto  ">
  <img src="../assets/1.png"  alt="">

</div>

    </form>
      
      
      </div>







      <div class="paginaB" v-else-if="seletorPage==1">
            <h1 class="mb-3 text-start">Sobre o Atendimento</h1>
            <h3 class="my-5 text-start">Detalhes do atendimento</h3>
              <form  class="row g-3 needs-validation ">
                <div class="col-md-6 ">
                  <label for="validationCustom01" class="form-label my-3">Especialidade principal*</label>
                  
                    <select class="form-select" aria-label="Default select example" v-model="especialidadeData" >
                    <option selected >Selecione a especialidade</option>
                    <option v-for="esp in especialidade" :key="esp" >{{esp.nome}}</option>
                    
                  </select>
        
                <label for="validationCustom05" class="form-label my-3">Informe o valor*</label>
                <div class="col-md-9">
                  
                  <div class="input-group mb-3 ">
                    <span class="input-group-text bck text-light">R$</span>
                    <input type="text" class="form-control" aria-label="Dollar amount (with dot and two decimal places)" v-model="valorData" required>
                  </div>
                </div>
        
        <label for="validationCustom05" class="form-label my-3">Formas de pagamento da consulta*</label>
        <div class="card shadow-sm my-3">
          <div class="card-body bck3">
            <div class="form-check">
              <input class="form-check-input " type="checkbox" name="flexRadioDefault" id="flexRadioDefault1" @click="dinheiro()">
                <label class="form-check-label " for="flexRadioDefault1">
                Em dinheiro
                </label>
            </div>
          </div>
        </div>

        <div class="card shadow-sm">
          <div class="card-body bck3">
            <div class="form-check ">
              <input class="form-check-input" type="checkbox" name="flexRadioDefault" id="flexRadioDefault1" @click="pix()">
                <label class="form-check-label" for="flexRadioDefault1">
                Pix
                </label>
            </div>
          </div>
        </div>

        <div class="card shadow-sm my-3">
          <div class="card-body bck3">
            <div class="form-check ">
              <input class="form-check-input" type="checkbox" name="flexRadioDefault" id="flexRadioDefault1" v-model="cartao" @click="credito()">
                <label class="form-check-label" for="flexRadioDefault1">
                Cartão de crédito
                </label>
            </div>
              <div class="" v-if="cartao">
              parcelemento em:

                <div class="form-check ">
                  <input class="form-check-input" type="radio" name="flexRadioDefault" id="flexRadioDefault1" @click="parcelado1()" >
                    <label class="form-check-label" for="flexRadioDefault1">
                    1x, sem juros
                    </label>
                </div>
                <div class="form-check ">
                  <input class="form-check-input" type="radio" name="flexRadioDefault" id="flexRadioDefault1" @click="parcelado2()">
                    <label class="form-check-label" for="flexRadioDefault1">
                    2x, sem juros
                    </label>
                </div>
                <div class="form-check ">
                  <input class="form-check-input" type="radio" name="flexRadioDefault" id="flexRadioDefault1" @click="parcelado3()">
                    <label class="form-check-label" for="flexRadioDefault1">
                    3x, sem juros
                    </label>
                </div>
              </div>
          </div>
        </div>

       
     
       

<div class="row justify-content-center my-5 ">
  <div class="bar col-md-6"></div>
  <div class="bar col-md-6"></div>
  
  <div class="col-md-3">
    <span class="">2 de 2</span>

  </div>

</div>



      </div>
<div class="col-md-6 my-auto  ">
  <img src="../assets/2.png"  alt="">

</div>

    </form>
      
      </div>






      <div class="paginaC" v-else-if="seletorPage==2">
      
<div class="row">
        <h1 class="mb-3 text-start ps-5">Revisão do cadastro</h1>


                  <div class=" col-md-6 text-start ps-5  my-4">

                   
                    <div class="revisao">
                    <li class="">

                      <ul class="fw-bold">Nome completo</ul>
                      <ul class="fw-normal mb-5">{{nomeData}}</ul>

                      <ul class="fw-bold">CPF</ul>
                      <ul class="fw-normal mb-5">{{cpfData}}</ul>

                      <ul class="fw-bold">Número de celular ou telefone</ul>
                      <ul class="fw-normal mb-5">{{telefoneData}}</ul>

                      <ul class="fw-bold">Estado/Cidade</ul>
                      <ul class="fw-normal mb-5">{{estadoData+cidadeData}}</ul>

                      <ul class="fw-bold">Especialidade principal</ul>
                      <ul class="fw-normal mb-5">{{especialidadeData}}</ul>

                      <ul class="fw-bold">Preço da consulta</ul>
                      <ul class="fw-normal mb-5">{{valorData}}</ul>

                      <ul class="fw-bold">Formas de pagamento da consulta</ul>
                      <ul class="fw-normal mb-5">{{pagamentoData+parcelas}}</ul>

                    </li>
                    </div>
                    
                

                   
                   

                    

                  </div>


            
                  <div class=" col-md-6  my-auto  ">

                    <img  src="../assets/3.png"   alt="imagem">

                  </div>
</div>
      
      </div>


      

      <div class="my-3 col-md-6 d-grid gap-2 bck rd " v-if="seletorPage==0 || seletorPage==1" >
        <button  class="btn text-light" type="submit" @click="f()">PRÓXIMO</button>
      </div>

      <div class="my-4 col-md-6 d-grid  bck2 rd " v-if="seletorPage==2" >
        <button  class="btn text-dark fw-bold" type="submit">CADASTRAR PROFISSIONAL</button>
      </div>

      <div>
        <a href="#" class="borda  fw-bold edCad" v-if="seletorPage==2" @click="seletorPage=0">Editar cadastro</a> 
      </div>

           
           
           </div>
    </div>

</div> 

</template>

<script>
import axios from 'axios'
export default {
  name: 'CadastroPage',
  props: {
    msg: String
   
  },
  data() {
    return {
      seletorPage:0,
      titulo: 'Sobre o professional',
      estado: [],
      cidade: [],
      cpf: [],
      especialidade: [],
      nomeData:"",
      cpfData:"",
      estadoData:"",
      cidadeData:"",
      telefoneData:"",
      valorData:"",
      especialidadeData:"",
      pagamentoData:"",
      cartao:false,
      parcelas:"",

      f:()=>{this.seletorPage+=1},
      v:()=>{this.seletorPage-=1},
      dinheiro:()=>{this.pagamentoData="em dinheiro"},
      pix:()=>{this.pagamentoData="pix"},
      credito:()=>{this.pagamentoData="cartão de credito"},
      parcelado1:()=>{this.parcelas="1x, sem juros"},
      parcelado2:()=>{this.parcelas="2x, sem juros"},
      parcelado3:()=>{this.parcelas="3x, sem juros"},
      
      
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
    axios
      .get('https://api-teste-front-end-fc.herokuapp.com/especialidades')
      .then(response => (this.especialidade = response.data))
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
  width: 95%;
}
</style>

<style scoped>
.rd{
  border-radius: 16px;
}
.bck{
  background-color: #483698;
}
.bck2{
  background-color: #FBDE40;
}
.bck3 {
  background-color: #F9F9F9;
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
.revisao {
  font-family: 'Open Sans', sans-serif;
  color: #282828;
}
.edCad {
  text-decoration: none;
  color: #483698 ;
}
.borda{
  border: 1px solid red;
}
</style>
