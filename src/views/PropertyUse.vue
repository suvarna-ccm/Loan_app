<template>
    <v-container>
        <section>
        <h2>How this property will be used?</h2>
        <v-row>
          <v-col class="d-flex"  cols="12" sm="2"> 
          <v-card><p id="prop_use1" @click="show">Primary Home</p></v-card>
          </v-col>

           <v-col class="d-flex"  cols="12" sm="2"> 
          <v-card><p id="prop_use2" @click="show">Secondary Home</p></v-card>
          </v-col>

           <v-col class="d-flex"  cols="12" sm="2"> 
          <v-card><p id="prop_use3" @click="show">Rental Home</p></v-card>
          </v-col>
        </v-row>
   <div class="link">   <router-link to="/property-loc">Next</router-link> </div>
          
       <!-- <property-loc></property-loc> -->

       </section>
    </v-container>
</template>

<script>
// import PropertyLoc from './PropertyLoc.vue'
export default {
  // components: {
  //    PropertyLoc,
  //    },
name:'PropertyUse',
methods:{
  show(){
    var clicked_id=(event.srcElement.id);
      var txt=document.getElementById(clicked_id).textContent;
      localStorage.setItem("prop_use",txt);
      // var prop_use=localStorage.getItem("prop_use");
      // console.log(prop_use);

  }
}
    
}
</script>