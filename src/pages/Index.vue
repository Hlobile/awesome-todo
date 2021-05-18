<template>
  <q-page padding >
    <!--bind v-model to message-->
    <!--add event button next to input,-->
    <input 
    v-model="message" 
    @keyup.esc="clearMessage"
    @keyup.enter="alertMessage"
    />
    <button @click= "clearMessage">Clear</button>
    <h5
     v-if="message.length"
     class="border-grey"
    >{{message}}</h5>
    <h6 v-else>No meesage was entered</h6>
  </q-page>
</template>

<script lang="ts">

import { Vue, Component } from 'vue-property-decorator';


export default{
   data(){
     return{
       message: "I love God"
     }
   },

   methods: {
     clearMessage(){
       this.message = ''
     },
      alertMessage(){
       alert(this.message)
     }

    // handleKeyup(e){
      // if(e.keyCode == 27){
        // this.clearMessage()
      // }
       //else if(e.keyCode == 13){
    //      this.alertMessage()
    //    }

    //  },
    
   }


}
  

</script>
<style>
 .border-grey{
   border:1px solid grey
 }
</style>