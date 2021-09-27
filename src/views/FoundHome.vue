<template>
    <v-main>
     <section>
         <div class="forms">
         <h2>Have you alreday found your new home</h2>
         <v-btn id="found_y" @click="show">Yes</v-btn>
         <v-btn id="found_n" @click="show">No</v-btn>
         <section>
         <h2>Are you currently working with a real state agent?</h2>
         <v-btn id="agent_y" @click="show">Yes</v-btn>
         <v-btn id="agent_n" @click="show">No</v-btn>
         </section>
       <div class="link"> <router-link to="/buy-home">Next</router-link> </div>
         </div>
         <!-- <buy-home></buy-home> -->
     </section>

    </v-main>
</template>

<script>
//import BuyHome from './BuyHome.vue'
export default {
  //components: { BuyHome },
    name:'FoundHome',
    methods:{
       show(){
      var clicked_id=(event.srcElement.id);
     var txt1=document.getElementById(clicked_id).textContent;
     localStorage.setItem("found_home",txt1);

      var txt2=document.getElementById(clicked_id).textContent;
      localStorage.setItem("state_agent",txt2);

     // var found_home=localStorage.getItem("found_home");
     // console.log(found_home);
      }
    }
}
</script>