<template>
    <v-main><section>
        <h2>What is your combined household income?</h2>
        <div class="forms">
            <v-form>
             <v-text-field @blur="show"></v-text-field>
             <span>Its ok to continue</span>
           <div class="link"> <router-link to="/employed">Next</router-link> </div>


            </v-form>
        </div>
        
        </section></v-main>
</template>

<script>
export default {
    name:'AnIncome',
    methods:{
     show(){
     var clicked_id=(event.srcElement.id);
     var txt=document.getElementById(clicked_id).value;
     localStorage.setItem("an_income",txt);
      }
    }
}
</script>