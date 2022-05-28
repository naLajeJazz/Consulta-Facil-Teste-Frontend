<template>
  <CadastroPage/>
  <PaginaA  msg="Sobre o Profissional"/>
  <PaginaB msg="Sobre o Profissional"/>
  <PaginaC msg="Sobre o Profissional"/>
</template>

<script>
import PaginaA from './components/PaginaA.vue'
import PaginaB from './components/PaginaB.vue'
import PaginaC from './components/PaginaC.vue'
import CadastroPage from './components/CadastroPage.vue'




export default {
  name: 'App',
  components: {
    PaginaA,
    PaginaB,
    PaginaC,
    CadastroPage
},
data() {
    return {
      page1: true
    }
  },

}
</script>

<style>


#app {
  font-family: 'Comfortaa', cursive, Helvetica, Arial, sans-serif;
  font-weight: bold;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #483698;
  margin-top: 60px;
  
}
body{
  background-color: #FFE766;
}
</style>
