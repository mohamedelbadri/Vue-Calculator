<template>
    
    <div>
        <h2>lets calculate</h2>
        <input  v-model="first" type="number" name="first#" placeholder="1st #">
        
         <!-- <select name="sign" v-model="sign">
               
                <option v-bind="sign" value="+">+</option>
                <option v-bind="sign" value="-">-</option>
                <option v-bind="sign" value="x">x</option>
                <option v-bind="sign" value="/">/</option>
                
            </select> -->

            <select v-model="sign">
                <option disabled value="">Please select one</option>
                
                <option>+</option>
                <option>-</option>
                <option>x</option>
                <option>/</option>
            </select>
            <input type="text" name="sign" v-model="sign" placeholder="sign( + or - or x or / )">
            
        <input  v-model="second" type="number" name="second#" placeholder="2nd #">

        <input type="submit" value="submit" v-on:click="getResult(first,second,sign)" > 
       
        <h5>Result =  {{result}}</h5>
    </div>

</template>

<script>

export default {
    name: 'Calculations',
    data() {
        return{
            first : 0,
            second :  0,
            result: '',
            plus: '+',
            minus: '-',
            multiply: 'x',
            divide: '/',
            sign: ''
        }
    },
    methods:  {
        getResult: function(one , two, signn) {
            if(signn === this.minus){
                this.result = parseInt(one) - parseInt(two)
            }
            else if(signn === this.multiply){
                this.result = parseInt(one) * parseInt(two)
            }
             else if(signn === this.divide){
                this.result = parseInt(one) / parseInt(two)
            }
             else if(signn === this.plus){
                this.result = parseInt(one) + parseInt(two)
            }
            else{
                this.result = 'error, please enter (+ or - or x or /)'
            }
        
          
           
        }

    }

}
</script>

<style scoped>

</style>


