<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <entrada @envia="recebe"></entrada>
    <resultado :dados="result"></resultado>
  </div>
</template>

<script>
import entrada from './components/entrada'
import resultado from './components/resultado'

export default {
  name: 'app',
  components: {
    'entrada': entrada,
    'resultado': resultado
  },
  data: function() {
    return{
      result: null,
    }
    
  },
  methods:{
    recebe(dados){
      this.result = dados;
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
