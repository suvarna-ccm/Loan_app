<template>
    <v-main>
        <section>
        <h2>In which city the property will be located?</h2>
        <div class="forms">
        <form>
            <v-text-field 
            label="City,State" 
            @blur="show" 
            :rules="[rules.required]"
            id="prop_loc"></v-text-field>
            <span>Please mention close by city</span>
            <div class="link" v-if="active"><router-link to="/found-home">Next</router-link></div> 

        </form>
        </div>


        </section>
    </v-main>
</template>

<script>
export default {
    name:'PropertyLoc',
    data(){
        return{
            active:false,
             rules:{
             required: value => !!value || 'Required.',
            },
        }
    },
    methods:{
        show(){
        var txt=document.getElementById("prop_loc").value;
        if(txt==null || txt==="")
        document.getElementsByClassName("v-messages")[1].innerHTML="Please enter the city"
        else{
          this.active=true
          document.getElementsByClassName("v-messages")[1].innerHTML="   "
          localStorage.setItem("prop_loc",txt);
            }


   
        }
    }
}
</script>

<style scoped>

</style>