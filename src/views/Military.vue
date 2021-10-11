<template>
    <v-main>
        <section>
<div class="forms">
          <h2>Have you or your spouse served in military</h2>
          <v-btn id="mil_y" @click="show">Yes</v-btn>
          <v-btn id="mil_n" @click="show">No</v-btn>
    <div class="link" v-if="active">    <router-link to="/bankruptcy">Next</router-link> </div>
</div>
        </section>
    </v-main>
</template>

<script>
export default {
    name:'Military',
    data(){
        return{
            active:false
        }
    },
    methods:{
    show(){
        this.active=true
      var clicked_id=(event.srcElement.id);
     var txt=document.getElementById(clicked_id).textContent;
     localStorage.setItem("military",txt);
         }

    }
}
</script>