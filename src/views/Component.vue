<script setup>
import FrontWheel from '@/components/FrontWheel.vue';  
import RearWheel from '@/components/RearWheel.vue';
</script>

<template>
    <h1>Component.vue</h1>
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