<template>
    <v-main><section>
        <h2>Estimate your Credit Score</h2>
        <v-btn id="excel" @click="show">Excellent (>=720)</v-btn>
        <v-btn id="good" @click="show">Good (680-720)</v-btn>
        <v-btn id="fair" @click="show">Fair (640-679)</v-btn>
        <v-btn id="poor" @click="show">Poor (less than 639)</v-btn>
        <h5>Dont't know your credit score.Get it free?</h5>
    <div class="link" v-if="active">    <router-link to="/born">Next</router-link> </div>
        </section></v-main>

</template>

<script>
export default {
    name:'CreditScore',
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
     localStorage.setItem("score",txt);
          }
   
        
    }
}
</script>

<style scoped>
h5{
    margin: 0.5em 0 0 0;
}
</style>