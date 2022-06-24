<template>
    <h1>Pegar valor</h1>
    <input type="number" id="valor1">
    <input type="number" id="valor2">
    <input type="submit" value="escreva algo">
    <p id="valorDigitado"></p>
    <p id="ValorDigitado2"></p>
    <select name="sinal" id="sinal">
      <option value="+">+</option>
      <option value="-">-</option>
      <option value="X">X</option>
      <option value="/">:</option>
    </select>
    <input type="button" value="=" @click="ativou" name="">
    <input type="text" name="result" id="Resu">
</template>

<script>

export default {
  name: 'App',
  data(){},
  methods:{
    ativou(){
    let sinal = document.getElementById("sinal").value;
    let valor1 = document.getElementById('valor1').value;
    let valor2 = document.getElementById('valor2').value;
    let resultado = document.getElementById("Resu");
    document.getElementById('valorDigitado').innerHTML = valor1;
    document.getElementById('ValorDigitado2').innerHTML = valor2;
    if(sinal == "+") resultado.value = parseInt(valor1) + parseInt(valor2);
    if(sinal == "-") resultado.value = parseInt(valor1) - parseInt(valor2);
    if(sinal == "X") resultado.value = parseInt(valor1) * parseInt(valor2);
    if(sinal == "/") resultado.value = parseInt(valor1) / parseInt(valor2);
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
