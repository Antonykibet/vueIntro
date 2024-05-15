<script setup>
    import {ref, onMounted} from 'vue'
    const input = ref(null)
    onMounted(()=>{
        input.value.focus()
    })
</script>
<template>
    <h1>Refs</h1>
    <input type="text" ref="input">
</template>