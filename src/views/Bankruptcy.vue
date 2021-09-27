<template>
    <v-main><section>
            <h2>Have you had a bankruptcy or foreclosure in the last 7 years</h2>
             <v-btn id="bankc_no" @click="show">NO</v-btn>
             <v-btn id="bankc" @click="show">Bankruptcy</v-btn>
             <v-btn id="forec" @click="show">Foreclosure</v-btn>
             <v-btn id="both" @click="show">Both</v-btn>
 <div class="link">   <router-link to="/long-foreclosure">Next</router-link> </div>

          </section></v-main>
</template>




<script>
export default {
    name:'Bankruptcy',
    methods:{
            show(){
      var clicked_id=(event.srcElement.id);
     var txt=document.getElementById(clicked_id).textContent;
     localStorage.setItem("bankruptcy",txt);
      }
    }
}
</script>