<template>
  <v-app>
        <v-app-bar app>
           <router-link to="/">    <v-img
        class="mx-2"
        :src="require('./assets/logo.png')" 
        max-height="64"
        max-width="64"
        contain
      ></v-img></router-link>
            <v-toolbar-title> <router-link to="/"> Welcome to Ezee Loan</router-link></v-toolbar-title>
            <nav>
    <ul>
      <li><router-link to="/">HOME</router-link></li>
      <li><router-link to="/about">ABOUT</router-link></li>
      <li><router-link to="/contact">CONTACT</router-link></li>

    </ul>
</nav>

              </v-app-bar>
        <v-container> 
                     <!-- <router-view></router-view> -->

       <intro></intro>
       <property-type></property-type>
      <div class="thanks"> 
<v-btn @click="show" color="Secondary" id="thanks_btn">
      Thanks for your time</v-btn></div>
     <div id="inputs" v-if="Active" >
         <p id="loan_txt"></p>
         <p id="prop_typ_txt"></p>
         <p id="prop_use_txt"></p>
         <p id="prop_loc_txt"></p>
         <p id="found_home_txt"></p>
         <p id="state_agent_txt"></p>
         <p id="pur_price_txt"></p>
         <p id="buy_home_txt"></p>
         <p id="down_pay_txt"></p>
         <p id="bank_acc_txt"></p>
         <p id="is_buy_txt"></p>
         <p id="is_coborrow_txt"></p>
         <p id="an_income_txt"></p>
         <p id="employed_txt"></p>
         <p id="score_txt"></p>
         <p id="military_txt"></p>
         <p id="bankruptcy_txt"></p>
         <p id="street_txt"></p>
         <p id="zip_txt"></p>
         <p id="city_txt"></p>
         <p id="f_name_txt"></p>
         <p id="l_name_txt"></p>
         <p id="email_txt"></p>
         <p id="mobile_txt"></p>
         <p id="ssn_txt"></p>

       </div>
       </v-container>

     </v-app>
</template>

<script>
// import AppNavigation from './components/AppNavigation.vue'
import Intro from './components/Intro.vue'
import PropertyType from './views/PropertyType.vue'

export default {
  components: {
//      AppNavigation,
     Intro,
     PropertyType,
    //  Rates,
    },
    data(){
          return{
             //   isActive:true,
                Active:false,
                flag:1,
          }
    },
    
    methods:{
      show(){
      this.Active=true

      var c25=localStorage.getItem("loan")
      document.getElementById("loan_txt").innerHTML="Type of Loan - "+c25  

        var c1=localStorage.getItem("prop_typ")
      document.getElementById("prop_typ_txt").innerHTML="Type of Home - "+c1  
        
        var c2=localStorage.getItem("prop_use")
      document.getElementById("prop_use_txt").innerHTML="Property Use - "+c2  
  
        var c3=localStorage.getItem("prop_loc")
      document.getElementById("prop_loc_txt").innerHTML="Property Location - "+c3  

        var c4=localStorage.getItem("found_home")
      document.getElementById("found_home_txt").innerHTML="Found Home - "+c4  

var c5=localStorage.getItem("state_agent")
      document.getElementById("state_agent_txt").innerHTML="State Agent - "+c5  

var c6=localStorage.getItem("pur_price")
      document.getElementById("pur_price_txt").innerHTML="Purchased Price - "+c6  

var c7=localStorage.getItem("buy_home")
      document.getElementById("buy_home_txt").innerHTML="Buy Home - "+c7  

var c8=localStorage.getItem("down_pay")
      document.getElementById("down_pay_txt").innerHTML="Down Payment - "+c8  

var c9=localStorage.getItem("bank_acc")
      document.getElementById("bank_acc_txt").innerHTML="Bank Account - "+c9  

var c10=localStorage.getItem("is_buy")
      document.getElementById("is_buy_txt").innerHTML="Is buy - "+c10  

var c11=localStorage.getItem("is_coborrow")
      document.getElementById("is_coborrow_txt").innerHTML="Is Co-borrower - "+c11  

var c12=localStorage.getItem("an_income")
      document.getElementById("an_income_txt").innerHTML="Annual Income - "+c12  

var c13=localStorage.getItem("employed")
      document.getElementById("employed_txt").innerHTML="Employed - "+c13  

var c14=localStorage.getItem("score")
      document.getElementById("score_txt").innerHTML="Credit score - "+c14  

var c15=localStorage.getItem("military")
      document.getElementById("military_txt").innerHTML="Served in military - "+c15  

var c16=localStorage.getItem("bankruptcy")
      document.getElementById("bankruptcy_txt").innerHTML="Bankrupt - "+c16  

var c17=localStorage.getItem("street")
      document.getElementById("street_txt").innerHTML="Street - " +c17  

var c18=localStorage.getItem("zip")
      document.getElementById("zip_txt").innerHTML="Zip - " +c18  

var c19=localStorage.getItem("city")
      document.getElementById("city_txt").innerHTML="City - " +c19  


var c20=localStorage.getItem("f_name")
      document.getElementById("f_name_txt").innerHTML="First Name - " +c20  

var c21=localStorage.getItem("l_name")
      document.getElementById("l_name_txt").innerHTML="Last Name - " +c21  

var c22=localStorage.getItem("email")
      document.getElementById("email_txt").innerHTML="Email - " +c22 

var c23=localStorage.getItem("mobile")
      document.getElementById("mobile_txt").innerHTML="Mobile - " +c23  

var c24=localStorage.getItem("ssn")
      document.getElementById("ssn_txt").innerHTML="SSN - " +c24  


      }
    },
 
}
</script>

<style lang="scss" >
.v-application .theme--light.v-app-bar.v-toolbar.v-sheet {
       background-color: deepskyblue;}
.v-application .v-toolbar__title a{color:#2c3e50}
li{display: inline;list-style: none;margin-right: 1em;}

.thanks{clear:both;float:right; margin-top:1em ;padding-bottom:1em ;}
#inputs{clear: both}
h2{padding-bottom: 1em;}
.v-card p{margin-top:1em}
.top-margin{margin-top:1em}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

section{margin-top:1em}
.container{margin-top:2em}
section .v-btn{margin-left:1em; border-radius: 25px;}
.padding-bottom{padding-bottom:1em ;}
#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
.v-card p{cursor: pointer;}
.forms{width:60%; margin: 0 auto;}
.link{float: right;margin:1em 0 0 0;}
 a{text-decoration: none;text-decoration-thickness: 40;}

 .slidecontainer {
  width: 100%; /* Width of the outside container */
}

/* The slider itself */
.slider {
  -webkit-appearance: none;  /* Override default CSS styles */
  appearance: none;
  width: 100%; /* Full-width */
  height: 10px; /* Specified height */
  background: #d3d3d3; /* Grey background */
  outline: none; /* Remove outline */
  opacity: 0.7; /* Set transparency (for mouse-over effects on hover) */
  -webkit-transition: .2s; /* 0.2 seconds transition on hover */
  transition: opacity .2s;
  border-radius:50px ;
  
}

/* Mouse-over effects */
.slider:hover {
  opacity: 1; /* Fully shown on mouse-over */
}

/* The slider handle (use -webkit- (Chrome, Opera, Safari, Edge) and -moz- (Firefox) to override default look) */
.slider::-webkit-slider-thumb {
  -webkit-appearance: none; /* Override default look */
  appearance: none;
  width: 20px; /* Set a specific slider handle width */
  height: 20px; /* Slider handle height */
  background: #04AA6D; /* Green background */
  cursor: pointer; /* Cursor on hover */
  border-radius: 50%;
}


</style>
