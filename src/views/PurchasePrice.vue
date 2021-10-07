<template>
    <v-main>
<section>
    <h2>What is the estimated purchase price?</h2>
        <div class="forms">
  <div class="slidecontainer">
  <input type="range" min="200000" @blur="show" max="250000" value="50" class="slider" id="myRange">

</div>
  <p><span>0 to 250000</span> Value: <span id="pur_price"></span></p>
     <!-- <v-btn @click="show">show value</v-btn>    -->
          <div class="link">    <router-link to="/down-payment">Next</router-link> </div>

        </div>


</section>

    </v-main>
</template>

<script>
export default {
    name:'PurchasePrice',
    data(){
      return{
        value:0,
      }
    },
    methods:{
      show(){
        var slider = document.getElementById("myRange");
        var output = document.getElementById("pur_price");
         output.innerHTML = "$" + slider.value; // Display the default slider value

// Update the current slider value (each time you drag the slider handle)
       slider.oninput = function() {
       output.innerHTML ="$" + this.value;
        }

        localStorage.setItem("pur_price",output.textContent);
      }
    }

}
</script>