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
         <div class="link" >  <router-link to="/property-use">Next</router-link> </div>

    </section>
 <!-- <keep-alive><component v-bind:is="PropertyUse" /></keep-alive> -->
        </v-main>
        
</template>



<script>
export default {
    name: 
    'PropertyType',
    methods:{
      show(){
      var clicked_id=(event.srcElement.id);
      var txt=document.getElementById(clicked_id).textContent;
      localStorage.setItem("prop_typ",txt);
           }

      //console.log(clicked_id)
      //  var myContent = document.getElementsByClassName("txt")[0].textContent;    
     // var myContent = document.getElementById("clicked_id").textContent;
      //console.log(clicked_id);

     //   var myContent = this.textContent;

       // console.log(myContent);
      //  localStorage.setItem("Suvarna", myContent);
     //   console.log(localStorage.getItem("myContent"))

      

     // console.log(.v-card.value)
     }
    }
        
  


</script>

<style>

</style>