<template>
    <v-main>
        <section>
            <div class="forms">
            <span>Providing your SSN is optional,but it will allow us to get more personalised rates.</span>
            <v-text-field id="ssn" @blur="show"></v-text-field>
            <label>(This will not effect your credit.Your SSN is to used 
            to verify your identity.</label>
            <div class="link"> <router-link to="/">Next</router-link> </div>

            </div>
        </section>
    </v-main>
</template>

<script>
export default {
    methods:{
        show(){
            var regexp=/^[2-9]{1}[0-9]{3}\s{1}[0-9]{4}\s{1}[0-9]{4}$/;
            var txt=document.getElementById("ssn").value;
            if(regexp.test(txt))
            {localStorage.setItem("ssn",txt)}

        }
    }
}
</script>