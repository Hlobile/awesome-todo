<template>
  <q-page padding >
    <input v-model="message" /><!--bind v-model to message-->
    <!--add event button next to input,-->
    <button @click= "message = ''">Clear</button>
    <h5>{{message}}</h5>
  </q-page>
</template>

<script lang="ts">

import { Vue, Component } from 'vue-property-decorator';


export default{
   data(){
     return{
       message: "I love God"
     }
   }


}
  

</script>
