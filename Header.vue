<template>
 
<div>
     <header class="header">
            <img src="favicon.ico" alt="vuelogo" class="vuelogo">
        <h3> <strong> This is a Calculator App</strong></h3>
       
    </header>
    <a  class="alt" href="https://calculator-1.com/">Real Calculator app</a>
    
</div>

   
</template>

<script>
export default {
   name: 'Header' 
}
</script>

<style scoped>
.header {
        background: #333;
        color: #fff;
        text-align: center;
       display: block;
       
  
      
    }
    .vuelogo {
       margin-top: 10px;
      }
      .alt {
          color: white;
          background-color: black;
      }
</style>
