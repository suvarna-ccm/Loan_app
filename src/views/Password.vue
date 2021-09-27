<template>
    <v-main>
        <section>
            <div class="forms">
            <h2>Great your rates are ready to view.Let's create your password 
            to save your progress</h2>
          <v-text-field
            :append-icon="show3 ? 'mdi-eye' : 'mdi-eye-off'"
            :rules="[rules.required, rules.min]"
            :type="show3 ? 'text' : 'password'"
            name="input-10-2"
            label="Not visible"
            hint="At least 8 characters"
            value="wqfasds"
            class="input-group--focused"
            @click:append="show3 = !show3"
            id="password"
            @blur="show"
          ></v-text-field>
     <div class="link">    <router-link to="/mobile">Next</router-link> </div>
            </div>
        </section>
    </v-main>
</template>


<script>
export default {
    name:'Password',
       data () {
      return {
        show1: false,
        show2: true,
        show3: false,
        show4: false,
        password: 'Password',
        rules: {
          required: value => !!value || 'Required.',
          min: v => v.length >= 8 || 'Min 8 characters',
          emailMatch: () => (`The email and password you entered don't match`),
        },
      }
    },
    methods:{
        show(){
            var txt=document.getElementById("password").value;
            console.log(txt);
        }
        
    }
}
</script>