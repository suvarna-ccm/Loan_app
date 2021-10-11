<template>
    <v-main>
        <section>
            <h2>What is your name</h2>
            <div class="forms">
                <v-text-field :rules="[rules.required]" placeholder="First Name" id ="f_name" @blur="show"></v-text-field>
                <v-text-field placeholder="Last Name" id ="l_name" @blur="show"></v-text-field>
            <div class="link" v-if="active">    <router-link to="/email">Next</router-link> </div>

            </div>
        </section>
    </v-main>
</template>

<script>
export default {
    name:'Name',
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
      var txt1=document.getElementById("f_name").value;
      var txt2=document.getElementById("l_name").value;
      if((txt1.length)>2) 
      this.active=true


    localStorage.setItem("f_name",txt1);
    localStorage.setItem("l_name",txt2);

    //  var bankruptcy=localStorage.getItem("bankruptcy");
      console.log(txt1);
      console.log(txt2);


    }
}
}
</script>