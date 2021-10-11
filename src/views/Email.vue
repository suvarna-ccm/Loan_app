<template>
    <v-main>
        <section>
            <div class="forms">
                        <h2>What is your Email</h2>
<v-text-field
            v-model="email"
            :rules="[rules.required, rules.email]"
            label="E-mail"
            id="email"
            @blur="show"
          ></v-text-field>
                    <p><span>We take your privacy seriously</span></p>
     <div class="link" v-if="active">    <router-link to="/password">Next</router-link> </div>
            </div>
        </section>
    </v-main>
</template>

<script>
export default {
    name:'Email',
    data(){
        return{
            email:'',
            active:false,
            rules:{
                          required: value => !!value || 'Required.',
            counter: value => value.length <= 20 || 'Max 20 characters',
            email: value => {
            const pattern = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
            return pattern.test(value) || 'Invalid e-mail.'
          },
            },


            }
        },
    
    methods:{
          show(){
            this.active=true
      var txt=document.getElementById("email").value;

    localStorage.setItem("email",txt);

    //  var bankruptcy=localStorage.getItem("bankruptcy");


    }
    }

}
</script>