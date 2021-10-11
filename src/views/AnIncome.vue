<template>
    <v-main><section>
        <h2>What is your combined household income?</h2>
        <div class="forms">
            <v-form>
             <v-text-field
              @blur="show"
              type="number"
              step="any"
              min="10000"
              counter
              ></v-text-field>
             <span>Please fill in digit only</span>
           <div class="link" v-if="active"> <router-link to="/employed">Next</router-link> </div>
   </v-form>
        </div>
        </section></v-main>
</template>

<script>
export default {
    name:'AnIncome',
    data(){
        return{
            active:false
        }
    },
    methods:{
     show(){
         this.active=true
         var clicked_id=(event.srcElement.id);
         var txt=document.getElementById(clicked_id).value;
         localStorage.setItem("an_income",txt);
      }
    }
}
</script>