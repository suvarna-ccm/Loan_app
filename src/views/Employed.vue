<template>
    <v-main>
        <section>
            <div class="forms">
            <h2>Are you currently employed</h2>
          <v-btn id="full" @click="show">Full-Time</v-btn>
          <v-btn id="part" @click="show">Part-Time</v-btn>
          <v-btn id="self" @click="show">Self-Employed</v-btn>
          <v-btn id="not_employed" @click="show">No, I am not employed</v-btn>
        
  <div class="link">   <router-link to="/credit-score">Next</router-link> </div>
</div>
</section>
    </v-main>
</template>

<script>
export default {
    name:'Employed',
    methods:{
    show(){
      var clicked_id=(event.srcElement.id);
     var txt=document.getElementById(clicked_id).textContent;
     localStorage.setItem("employed",txt);
      }
        
    }
}
</script>