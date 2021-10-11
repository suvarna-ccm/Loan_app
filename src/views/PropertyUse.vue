<template>
    <v-container>
        <section>
        <h2>How this property will be used?</h2>
        <v-row>
          <v-col class="d-flex"  cols="12" sm="3"> 
          <v-btn id="prop_use1" @click="show">Primary Home</v-btn>
          </v-col>

           <v-col class="d-flex"  cols="12" sm="3"> 
          <v-btn id="prop_use2" @click="show">Secondary Home</v-btn>
          </v-col>

           <v-col class="d-flex"  cols="12" sm="6"> 
          <v-btn  id="prop_use3" @click="show">Rental Home</v-btn>
          </v-col>
        </v-row>
   <div class="link" v-if="active">   <router-link to="/property-loc">Next</router-link> </div>
          
       <!-- <property-loc></property-loc> -->

       </section>
    </v-container>
</template>

<script>
// import PropertyLoc from './PropertyLoc.vue'
export default {
  data(){
    return{
      active:false,
    }
  },
name:'PropertyUse',
methods:{
  show(){
    this.active=true
    var clicked_id=(event.srcElement.id);
      var txt=document.getElementById(clicked_id).textContent;
      localStorage.setItem("prop_use",txt);
      // var prop_use=localStorage.getItem("prop_use");
      // console.log(prop_use);

  }
}
    
}
</script>
<style scoped>
/* .v-sheet.v-card{border-radius: 50%; padding: 1em} */
</style>