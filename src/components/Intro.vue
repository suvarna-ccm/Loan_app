<template>
<v-main>
<div id="intro_section">    
    <h2>Personal Loans for 2021</h2>
<h2>Compare Rates and Offers from Top Lenders</h2>
<v-row>
<v-col class="d-flex"  cols="12" sm="6">
        <v-select
          v-model="select"
          :hint="`${select.loan}`"
          :items="items"
          item-text="loan"
          item-value="abbr"
          label="Loan Purpose"
          persistent-hint
          return-object
          single-line
          @dblclick="show"
        ></v-select>
<!-- <p>{{select}}</p> -->
</v-col>
<v-col
        class="d-flex"
        cols="12"
        sm="6"
        
      >
<router-link to="/rates" class="top-margin">See Personalised Rates</router-link> 

</v-col>
</v-row>
<!-- <rates v-bind:class="{display: isDisplay}"></rates> -->
<!-- <rates>h</rates> -->

</div>
</v-main>
</template>

<script>
// import Rates from '../views/Rates.vue'
export default {
    name: 'Intro',
    // components:{Rates},
    data () {
      return {
        select: { state: 'Florida'},
        items: [
          { loan: 'Home Loan'},
          { loan: 'Maintainance Loan' },
        ],
      }
    },
    methods:{
    show(){
   //   alert("hi")
    //  var clicked_id=(event.srcElement.id);
      var txt=document.getElementsByClassName("v-messages__message")[0].textContent;
      alert(txt);
      localStorage.setItem("loan",txt);
     // this.isDisplay=true;
     // console.log(this.isDisplay)
    }
    }
    
};
</script>

<style scoped>
#intro_section{width:60%; margin: 0 auto;background: palegreen;padding: 2em;}
</style>