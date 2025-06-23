<script setup>
import FrontWheel from '@/components/FrontWheel.vue';  
import RearWheel from '@/components/RearWheel.vue';
import { useCounterStore } from '@/stores/counter.js';

const counterStore = useCounterStore(); 
</script>

<template>
    <h1>Component.vue</h1>
    <button @clivk="counterStore.increment">회전</button>
       <div class="wide">
        <FrontWheel></FrontWheel>
         <FrontWheel></FrontWheel>

       </div> 
       <div class = "wide">
          <RearWheel></RearWheel>
          <RearWheel></RearWheel>
       </div>
    
    
    
   
</template>

<style scoped>
.wide{display: flex;}

</style>