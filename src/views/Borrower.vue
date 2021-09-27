<template>
    <v-main>
        <div class="forms">
        <section>
            
         <h2>Is this first time buying a home?</h2>
         <v-btn id="buyhome_y" @click="show">Yes</v-btn>
         <v-btn id="buyhome_n" @click="show">No</v-btn>
        </section>
         <section>
         <h2>Will you have a co-borrower</h2>
         <v-btn id="borrower_y" @click="show1">Yes</v-btn>
         <v-btn id="borrower_n" @click="show1">No</v-btn>
         
     <div class="link">    <router-link to="/an-income">Next</router-link> </div>
        
   
      </section>
        </div>
        </v-main>
</template>

<script>
export default {
    name:'Borrower',
    methods:{
      
    show(){
     var clicked_id=(event.srcElement.id);

     var txt1=document.getElementById(clicked_id).textContent;
     localStorage.setItem("is_buy",txt1);

    


     

      },
    
    show1(){
             var clicked_id=(event.srcElement.id);
     var txt2=document.getElementById(clicked_id).textContent;
     localStorage.setItem("is_coborrow",txt2);
   



    },  
}
}
</script>