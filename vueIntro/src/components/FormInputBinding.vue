<script setup>
    import {ref} from 'vue'
    const value = ref('')
    const checked = ref(false)
    const checkedBoxes = ref([])
</script>
<template>
    <h1>Form Input Binding</h1>
    <h3>Text input</h3>
    <input type="text" v-model="value">
    <p>Entered value:{{ value }}</p>
    <h3>Check box</h3>
    <input type="checkbox" v-model="checked">
    <Label>{{ checked }}</Label>
    
    <h3>Multiple checkbox</h3>
    <input type="checkbox" id="eat" value="Eat" v-model="checkedBoxes">
    <label for="eat">Eat</label> <br>
    <input type="checkbox" id="sleep" value="Sleep" v-model="checkedBoxes">
    <label for="sleep">Sleep</label> <br>
    <input type="checkbox" id="code" value="Code" v-model="checkedBoxes">
    <label for="code">Code</label> <br>
    <input type="checkbox" id="repeat" value="Repeat" v-model="checkedBoxes">
    <label for="repeat">Repeat</label> <br>
    <p>Selected boxes: {{ checkedBoxes }}</p>

    <h3>Select</h3>
    <select name="" id="" v-model="selected">
        <option value="Eat"></option>
    </select>
</template>