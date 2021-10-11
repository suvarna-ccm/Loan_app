<template>
    <v-main>
        <section>
            <div class="forms">
            <h2>When do u plan to buy a new home?</h2>
            <p><v-btn id="btn1" @click="show" color="primary">Already under contract</v-btn></p>
            <p><v-btn id="btn2" @click="show" color="primary">Immidiately I am asking an offer</v-btn></p>
            <p><v-btn id="btn3" @click="show" color="primary">I'm shopping and considering few options</v-btn></p>
            <p><v-btn id="btn4" @click="show" color="primary">Within next couple months</v-btn></p>
        <!-- <purchase-price></purchase-price> -->
      <div class="link" v-if="active">   <router-link to="/purchase-price">Next</router-link> </div>
            </div>
        </section>
    </v-main>
</template>

<script>
// import PurchasePrice from './PurchasePrice.vue'
export default {
//   components: { PurchasePrice },
    name:'BuyHome',
    data(){
        return{
            active:false,
        }
    },
    methods:{
        show(){
            this.active=true
             var clicked_id=(event.srcElement.id);
     var txt=document.getElementById(clicked_id).textContent;
     localStorage.setItem("buy_home",txt);

        }
    }
}
</script>