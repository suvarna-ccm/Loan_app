<template>
    <v-main>
        <section>
            <h2>What is your current address</h2>
        <div class="forms">
<v-text-field id="street" :rules="[rules.required]"
  placeholder="Street Address"></v-text-field>
<v-text-field id="zip" :rules="[rules.required]" placeholder="Enter zip"></v-text-field>
<v-text-field id="city" @click="show" placeholder="City"></v-text-field>

           <div class="link">     <router-link to="/name"  >Next</router-link> </div>

        </div>

        </section>
    </v-main>
</template>

<script>
export default {
    name:'Address',
    data(){
        return{
            rules:{
             required: value => !!value || 'Required.',

            },
        }
    },
    methods:{
            show(){
    //  var clicked_id=(event.srcElement.id);
      var txt1=document.getElementById("street").value;
      var txt2=document.getElementById("zip").value;
      var txt3=document.getElementById("city").value;


    localStorage.setItem("street",txt1);
    localStorage.setItem("zip",txt2);
    localStorage.setItem("city",txt3);

    },
    
    }
}
</script>