<template>
    <v-main>
        <section>
          <div class="forms">
<h2>Check all that apply</h2>
<div class="forms">
<v-checkbox label="WellsFargo" color="primary" v-model="selected"
 @click="show"
  value="WellsFargo" hide-details></v-checkbox>
  
<v-checkbox  label="BankOfAmerica" color="primary" v-model="selected"
 @click="show" value="BankOfAmerica" hide-details></v-checkbox>
  
<v-checkbox  label="CityBank" color="primary" v-model="selected"
@click="show" value="CityBank" hide-details></v-checkbox>
  
<v-checkbox  label="SBI" color="primary" v-model="selected"
 @click="show"  value="SBI" hide-details></v-checkbox>
  
<v-checkbox  label="US Bank" color="primary" v-model="selected"
 @click="show" value="US Bank" hide-details></v-checkbox>
  
<v-checkbox  label="Chase" color="primary" v-model="selected"
   @click="show" value="Chase" hide-details></v-checkbox>
  
<v-checkbox  label="USAA" color="primary" v-model="selected"
 @click="show" value="USAA" hide-details></v-checkbox>
  
<v-checkbox  label="Ally Bank" color="primary" v-model="selected"
@click="show" value="Ally Bank" hide-details></v-checkbox>

  
<v-checkbox  label="None of these" color="primary" v-model="selected"
 @click="show" value="None of these" hide-details></v-checkbox>

<p id="bank_acc" class="display">{{selected}}</p>
<div class="link"><router-link to="/borrower">Next</router-link></div> 
<span><router-link to="/borrower">Skip this step</router-link></span>




</div>
          </div>
        </section>
    </v-main>
</template>

<script>
export default {
    name:'BankAccount',
    data(){
      return{
        selected:[]
      }
    },
    methods:{
      show(){
        var txt=document.getElementById("bank_acc").textContent
        localStorage.setItem("bank_acc",txt)
      }
    }
}
</script>
<style scoped>
.display{
  display: none;
}
</style>