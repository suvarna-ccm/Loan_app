<template>
    <v-main>
        <section>
        <h2>In which city the property will be located?</h2>
        <div class="forms">
        <form>
            <v-text-field label="City,State" @blur="show" id="prop_loc"></v-text-field>
            <span>If your city is not listed, please mention close by city</span>
            <div class="link"><router-link to="/found-home">Next</router-link></div> 

            <!-- <v-btn><v-icon>mdi-arrow-right</v-icon>Con</v-btn> -->
        </form>
        </div>

        <!-- <found-home></found-home> -->

        </section>
    </v-main>
</template>

<script>
//import FoundHome from './FoundHome.vue'
export default {
 // components: { FoundHome },
    name:'PropertyLoc',
    methods:{
        show(){
        var txt=document.getElementById("prop_loc").value;
        localStorage.setItem("prop_loc",txt);
       // console.log(txt)


   
        }
    }
}
</script>

<style scoped>

</style>