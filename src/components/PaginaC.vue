<template>
 
    <div class="container">

          <div class="card mx-5 mb-5 p-3 shadow rd">
            <div class="card-body row">
              
              <h1 class="mb-3 text-start">{{titulo}}</h1>

                  <div class=" col-md-6">

                    <ul class="list-group text-start">
                      <li class="list-group-item">An item</li>
                      <li class="list-group-item">A second item</li>
                      <li class="list-group-item">A third item</li>
                      <li class="list-group-item">A fourth item</li>
                      <li class="list-group-item">And a fifth one</li>
                    </ul>

                    
                    
                   
                    <div class="my-3 col-md-12 d-grid gap-2 bck rd " >
                      <button  class="btn text-dark fw-bold" type="submit">CADASTRAR PROFISSIONAL</button>
                    </div>

                    <div>
                     <a href="" class="fw-bold">Editar cadastro</a> 
                    </div>

                  </div>

                  <div class=" col-md-6 ">

                    <img src="../assets/3.png" width="90%" alt="">

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
      titulo: 'Revisão do cadastro'
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
label{
  font-family: 'Open Sans', sans-serif;
  color: #282828;
}
</style>

<style scoped>
.rd{
  border-radius: 25px;
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
