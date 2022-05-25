<template>
  
  <HelloWorld msg="Sobre o Profissional"/>
  <PaginaB msg="Sobre o Profissional"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import PaginaB from './components/PaginaB.vue'


export default {
  name: 'App',
  components: {
    HelloWorld,
    PaginaB
    
}
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
