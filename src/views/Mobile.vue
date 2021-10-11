
 
<template>
    <v-main>
        <section>
            <h2>Mobile or phone Number</h2>
<div class="forms">
              <v-text-field
              type="number"
              step="any"
              placeholder="Phone Number"
             :counter="10"
             @blur="show"
             id="mobile"
             :rules="[mobRule]"
        ></v-text-field>
         <div class="link">       
  <router-link to="/security-number">view my rates</router-link> </div>

</div>
        </section>
    </v-main>
</template>

<script>
export default {
    name:'Mobile',
    data(){
        return{
        mobRule:val =>{
            if(val.length>10) 
            return "Please enter 10 digit phone number"
        }
        }
    },
    methods:{
      show(){
             var txt=document.getElementById("mobile").value;
             localStorage.setItem("mobile",txt);
        }
    }
}
</script>