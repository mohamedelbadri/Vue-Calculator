<template>
  <div id="app">
    <Header />
    <h4>Large, easy and convenient online calculator</h4>
    <p>Use for work, school or personal calculations.
       You can make not only simple math calculations and calculation of interest on the loan and bank lending rates, 
       the calculation of the cost of works and utilities.Commands for the online calculator you can enter not only the mouse,
        but with a digital computer keyboard. Detailed instructions for using the calculator, see below.</p>
     <img class="calc" alt="Calc logo" src="https://images-na.ssl-images-amazon.com/images/I/81-d0FG6XXL._SX425_.jpg">
     <div class="bg"></div>
    <div class="bg bg2"></div>
    <div class="bg bg3"></div>

  <Calculations />
  </div>
  
</template>

<script>
import Calculations from './components/Calculations'
import Header from './components/Header.vue'


export default {
  name: 'app',
  components: {
    Header,
    Calculations
  }
  
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #4b502c;
  margin-top: 5px;
}
.calc {
  margin-top: 30px;
  width: 150px;
  height: 200px;
}

html {
  height:100%;
}

body {
  margin:0;
}

.bg {
  animation:slide 3s ease-in-out infinite alternate;
  background-image: linear-gradient(-60deg, #6c3 50%, #09f 50%);
  bottom:0;
  left:-50%;
  opacity:.5;
  position:fixed;
  right:-50%;
  top:0;
  z-index:-1;
}

.bg2 {
  animation-direction:alternate-reverse;
  animation-duration:4s;
}

.bg3 {
  animation-duration:5s;
}

.content {
  background-color:rgba(255,255,255,.8);
  border-radius:.25em;
  box-shadow:0 0 .25em rgba(0,0,0,.25);
  box-sizing:border-box;
  left:50%;
  padding:10vmin;
  position:fixed;
  text-align:center;
  top:50%;
  transform:translate(-50%, -50%);
}

h1 {
  font-family:monospace;
}

@keyframes slide {
  0% {
    transform:translateX(-25%);
  }
  100% {
    transform:translateX(25%);
  }
}
</style>
