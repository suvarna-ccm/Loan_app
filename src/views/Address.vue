<template>
    <v-main>
        <section>
            <h2>What is your current address</h2>
        <div class="forms">
<v-text-field id="street"
   :rules="[required]"
  placeholder="Street Address">
  </v-text-field>
  
   <v-text-field
   id="zip"
              type="number"   
              step="any"
              min="000000"
              ref="input"
              :rules="[numberRule]"
              v-model.number="number"
              placeholder="Enter zip"
            ></v-text-field>

<v-text-field 
id="city" 
  :rules="[required]"
 @click="show" placeholder="City"></v-text-field>

           <div class="link" v-if="active">     <router-link to="/name"  >Next</router-link> </div>

        </div>

        </section>
    </v-main>
</template>

<script>
export default {
    name:'Address',
    data(){
        return{
            active:false,
            txt1:String,
            txt2:String,
            txt3:String,
            required: value => !!value || 'Required.',
            numberRule: val => {
      if(val < 0) return 'Please enter a positive number'
      if(val.length>6) return 'Please enter 6 digit code'
      return true
    }

        }
    },
    methods:{
    show(){
        this.txt1=document.getElementById("street").value
        this.txt2=document.getElementById("zip").value
        this.txt3=document.getElementById("city").value

    if((this.txt3.length)>2)    this.active=true
    localStorage.setItem("street",this.txt1);
    localStorage.setItem("zip",this.txt2);
    localStorage.setItem("city",this.txt3);

    },
    
    }
}
</script>

<style scoped>
.theme--light.v-messages {
color: green;}
</style>