<script setup>
    import { ref } from 'vue'
    
    const count = ref(0)
    function increement(){
        count.value++
    }
</script>

<template>
    <button v-on:click="increement" >{{ count }}</button>
</template>