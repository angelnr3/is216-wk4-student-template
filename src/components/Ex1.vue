<script setup>
    import { ref } from 'vue'

    // Add code here
    // challenge: use array  
    const message = ref("Choose your favourite: ");
    const fruits = ref(["apple", "orange", "peach"]);
    
</script>

<template>
    {{ message }} 
   
    <!--<label for=""> <input type="radio" name="fruit"> {{ fruits[0] }} </label> 
    this method requires manual additions per fruit via each index [1], [2]
    instead, -->
    
    <label v-for="fruit in fruits" :key ="fruit">
        <input type="radio" name="fruit" :value="fruit">{{fruit}}
    </label>
    
</template>

<style scoped>
</style>
