<template>
    <v-main>
     <section>
         <div class="forms">
         <h2>Have you alreday found your new home</h2>
         <v-btn id="found_y" @click="show1">Yes</v-btn>
         <v-btn id="found_n" @click="show1">No</v-btn>
         <section>
         <h2>Are you currently working with a real state agent?</h2>
         <v-btn id="agent_y" @click="show">Yes</v-btn>
         <v-btn id="agent_n" @click="show">No</v-btn>
         </section>
       <div class="link" v-if="active"> <router-link to="/buy-home">Next</router-link> </div>
         </div>
         <!-- <buy-home></buy-home> -->
     </section>

    </v-main>
</template>

<script>
//import BuyHome from './BuyHome.vue'
export default {
    name:'FoundHome',
    data(){
      return{
        active:false,
      }
    },
    methods:{
      show1(){
            var clicked_id=(event.srcElement.id);
            var txt1=document.getElementById(clicked_id).textContent;
            localStorage.setItem("found_home",txt1);  
      },
       show(){
         this.active=true
      var clicked_id=(event.srcElement.id);
    //  var txt1=document.getElementById(clicked_id).textContent;
    //  localStorage.setItem("found_home",txt1);

      var txt2=document.getElementById(clicked_id).textContent;
      localStorage.setItem("state_agent",txt2);

     // var found_home=localStorage.getItem("found_home");
     // console.log(found_home);
      }
    }
}
</script>