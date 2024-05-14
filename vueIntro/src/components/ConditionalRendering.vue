<script setup>
    import {ref} from 'vue'
    const seen = ref(false)
</script>

<template>
    <h1>Conditional Rendering</h1>
    <h3>v-if</h3>
    <p v-if="seen">Do i see you...</p>
    <h3 >v-else</h3>
    <p v-if="seen">Do i see you...</p>
    <p v-else>No I dont...</p>
</template>