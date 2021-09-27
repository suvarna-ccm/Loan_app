<template>
    <v-main>
        <section>

            <h2>How long was the foreclosure</h2>
            <div class="forms"> <div class="slidecontainer">
  <input type="range" min="0" @blur="show" max="7" value="5"
   class="slider" id="myRange">
</div>
  <p>Value: <span id="long_forclosure"></span></p>
<div class="link"><router-link to="/address">Next</router-link> </div></div>

        </section>
    </v-main>
</template>

<script>
export default {
    name:'LongForeclosure',
    data(){
        return{
            value:0,
        }
    },
    methods:{
         show(){
        var slider = document.getElementById("myRange");
        var output = document.getElementById("long_forclosure");
         output.innerHTML = slider.value +" Years"; // Display the default slider value

// Update the current slider value (each time you drag the slider handle)
       slider.oninput = function() {
       output.innerHTML =this.value +" Years";
        }

        localStorage.setItem("long_forclosure",output.textContent);
      }
    


    }
}
</script>