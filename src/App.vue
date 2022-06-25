<template>
    <div class="Calculadora">
          <h1>Vueladora</h1>
    <div id="Table">
    <input type="number" id="valor1">
      <select name="sinal" id="sinal" >
      <option value="+">+</option>
      <option value="-">-</option>
      <option value="X">X</option>
      <option value="/">/</option>
      <option value="%">%</option> 
    </select>
    <input type="number" id="valor2">
        </div>
    <input type="button" value="=" @click="ativou" id="igual">
    <br>
     <input type="text" name="result" id="resultado"/>
      </div>
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
    let resultado = document.getElementById("resultado");
    if(sinal == "+") resultado.value = parseFloat(valor1) + parseFloat(valor2);
    if(sinal == "-") resultado.value = parseFloat(valor1) - parseFloat(valor2);
    if(sinal == "X") resultado.value = parseFloat(valor1) * parseFloat(valor2);
    if(sinal == "/") resultado.value = parseFloat(valor1) / parseFloat(valor2);
    if(sinal == "%") resultado.value = parseFloat(valor1) % parseFloat(valor2);
    }
}
}
</script>

<style>
body{
  text-align: center;
  background: linear-gradient(32deg,red,blue);
  background-repeat: no-repeat;
  background-position: center;
  height: 100vh;
  overflow: hidden;
  background-size: cover;
  color: white;
}
input[type="number"]::-webkit-outer-spin-button,
input[type="number"]::-webkit-inner-spin-button{
    -webkit-appearance: none;
    margin: 0;
}
#Table{
  display: flex;
}
#igual{
  border: 1px solid blue;
  background-color: blue;
  color: white;
  margin-top: 120px;
    font-size: 40px;
  border-radius: 10px;
  width: 10em;
  height: 2em;
}
select{
  -webkit-appearance: none;
  text-align: center;
  border: 1px solid red;
  background-color: red;
  color: white;
  border-radius: 50%;
  font-size: 40px;
  height: 2em;
  width: 2em;
}
input[type="number"] {
    -moz-appearance: textfield;
    width: 14em;
    height: 4em;
    display: flex;
    margin: auto;
    text-align: center;
    border-radius: 20px;
    border: 4px solid black;
    color: black;
    background: wheat;
}
.Calculadora{
  border: 4px solid black;
  width: 40em;
  height: 40em;
  border-radius: 20px;
  margin: auto;
  margin-top: 100px;
}
#resultado{
  margin: auto;
  margin-top: 20px;
  height: 4em;
  text-align: center;
  background: transparent;
  border: 1px solid transparent;
  color: white;
  font-size: 50px;
}
</style>
