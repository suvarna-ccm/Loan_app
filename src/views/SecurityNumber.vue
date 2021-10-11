<template>
    <v-main>
        <section>
            <div class="forms">
                <h2>Social Security</h2>
            <span>Providing your SSN is optional,but it will allow us to get more personalised rates.</span>
            <v-text-field 
            :counter="14"
            step="any"
            id="ssn" 
            :rules="[ssnRule]"
            @blur="show"></v-text-field>
            <label>(This will not effect your credit.Your SSN is to used 
            to verify your identity.</label>
   </div>
        </section>
    </v-main>
</template>

<script>
export default {
    data(){
        return{
            active:false,
            IsActive:false,
            ssnRule:val =>{ 
                if(val.match(/^[2-9]{1}[0-9]{3}\s{1}[0-9]{4}\s{1}[0-9]{4}$/))
                 return true
                 else if((val.length)>14)
                 return "Please enter 12 digit only with 2 space"
                 else if(val.match(/[a-zA-z]$/))
                return "Please enter digit or space only"
                else
                 return "Please enter in adhar number format with 1 space"
            }
        }
    },
    methods:{
        show(){
            var txt=document.getElementById("ssn").value;
            if(txt.length==14)
              this.active=true
            localStorage.setItem("ssn",txt)

        }
    }
}
</script>