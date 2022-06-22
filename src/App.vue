<template>
    <h1>Pegar valor</h1>
    <input type="number" id="valor1">
    <input type="number" id="valor2">
    <input type="submit" @click="ativou" value="escreva algo">
    <p id="valorDigitado"></p>
    <p id="ValorDigitado2"></p>
    <button @click="mais">+</button>
    <button @click="menos">-</button>
    <p id="somar"></p>
</template>

<script>

export default {
  name: 'App',
  data(){},
  methods:{
    ativou(capturando = "",Capturando = ""){
    capturando = document.getElementById('valor1').value;
    Capturando = document.getElementById('valor2').value;
    document.getElementById('valorDigitado').innerHTML = capturando;
    document.getElementById('ValorDigitado2').innerHTML = Capturando;
    },
    mais(capturando = "",Capturando = ""){
      
        var soma = parseInt(capturando) + parseInt(Capturando);
    document.getElementById('somar').innerHTML = soma;
    }
    }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
