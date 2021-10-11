<template>
    <v-main>
    <section>    
    <h2 id="title">What type of Property are u Purchasing?</h2>
     <v-row>
    <v-col class="d-flex"  cols="12" sm="3">    
    <v-card>
       <p id="prop_typ1" @click="show()"> Single Family Home</p>
        <v-img
             :src="require('../assets/home1.jpeg')" 
               class="my-3"
               contain
      height="200" />
    </v-card>
    </v-col>

    <v-col class="d-flex"  cols="12" sm="2">    
     <v-card>
       <p id="prop_typ2" @click="show()">Town Home</p>
          <v-img
             :src="require('../assets/home2.jpg')" 
               class="my-3"
               contain
      height="200" />
 
    </v-card>
    </v-col>

    
    <v-col class="d-flex"  cols="12" sm="2">    
     <v-card>
       <p id="prop_typ3" @click="show()">Condominium</p>
     <v-img
             :src="require('../assets/home3.jpg')" 
               class="my-3"
               contain
      height="200" />

     </v-card>
    </v-col>

    
    <v-col class="d-flex"  cols="12" sm="2">    
     <v-card>
       <p id="prop_typ4" @click="show()">MultiFamily Home</p>
 <v-img
             :src="require('../assets/home4.jpeg')" 
               class="my-3"
               contain
      height="200" />     </v-card>
    </v-col>


    
    <v-col class="d-flex"  cols="12" sm="3">    
     <v-card>
       <p id="prop_typ5" @click="show()">Manufactured Home</p>
<v-img
             :src="require('../assets/home5.jpg')" 
               class="my-3"
               contain
      height="200" />
     </v-card>
    </v-col>


    </v-row>  
         <div class="link" v-if="active">  <router-link to="/property-use">Next</router-link> </div>

    </section>
     <router-view></router-view>
        </v-main>
        
</template>



<script>
export default {
    name: 
    'PropertyType',
    data(){
      return{
        active:false
      }
    },
    
    methods:{
      show(){
        this.active=true;
      var clicked_id=(event.srcElement.id);
      var txt=document.getElementById(clicked_id).textContent;
      localStorage.setItem("prop_typ",txt);
      var prop_typ=localStorage.getItem("prop_typ");
      console.log(prop_typ);
      }

     
     }
    }
        
  


</script>

<style>

</style>