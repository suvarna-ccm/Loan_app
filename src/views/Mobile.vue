
 
<template>
    <v-main>
        <section>
            <h2>Mobile or phone Number</h2>
<div class="forms">
              <v-text-field
              placeholder="Phone Number"
          :counter="10"
          label="Phone Number"
          @blur="show"
          id="mobile"
        ></v-text-field>
         <div class="link">         <router-link to="/security-number">view my rates</router-link> </div>

</div>
        </section>
    </v-main>
</template>

<script>
export default {
    name:'Mobile',
    methods:{
        show(){
              var txt=document.getElementById("mobile").value;
             localStorage.setItem("mobile",txt);
        }
    }
}
</script>