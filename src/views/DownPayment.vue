<template>
    <v-main>
        <section>
            <div class="forms">
            <h2>How much are u putting down as a down payment?</h2>
            <div class="forms">
               
  <div class="slidecontainer">
  <input type="range" min="00%" @blur="show" max="90%" value="50" class="slider" id="myRange">
</div>
  <p><span>0 to 90%</span> Value: <span id="down_pay"></span></p>
        </div>
         <div class="link">       <router-link to="/bank-account">Next</router-link> 
         </div></div>
        </section>
    </v-main>
</template>


<script>
export default {
    name:'Down-Payment',
    methods:{
        show(){
              var slider = document.getElementById("myRange");
        var output = document.getElementById("down_pay");
         output.innerHTML = slider.value + "%"; // Display the default slider value

// Update the current slider value (each time you drag the slider handle)
       slider.oninput = function() {
       output.innerHTML = this.value + "%";
        }

        localStorage.setItem("down_pay",output.textContent); 
        }
    }
}
</script>