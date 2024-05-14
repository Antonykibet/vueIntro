<script setup>
    import {ref, reactive} from 'vue'
    const isHidden = ref(false)
    const errorOccur = ref(true)

    const styles = reactive({
        hide:false,
        error:true
    })
    const styleObject = reactive({
        color: 'red',
        fontSize: '10px'
    })
</script>

<template>
    <h1>Class and Style Binding</h1>
    <h3>Using Ref</h3>
    <p class="general" :class="{hide:isHidden,error:errorOccur}">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
    <h3>Using Reactive</h3>
    <p class="general" :class="styles" @click="styles.error=false" >Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
    <h3>Array</h3>
    <p  :class="[general, error]" >Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
    <h2>Style</h2>
    <p :style="styleObject">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Fugiat, corporis?</p>

</template>

<style>
    .general{
        font-style: italic;
    }
    .hide{
        display: none;
    }
    .error{
        color: rgb(199, 0, 0);
    }
</style>