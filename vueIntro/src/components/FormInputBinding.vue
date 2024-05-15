<script setup>
    import {ref} from 'vue'
    const value = ref('')
    const checked = ref('')
    const checkedBoxes = ref([])
    const selected = ref('')
    const lazyModifier = ref('')
    const numberModifier = ref('')
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
    <select  v-model="selected">
        <option>Eat</option>
        <option>Sleep</option>
        <option>Code</option>
        <option>Repeat</option>
    </select>
    <p>Selected option: {{ selected }}</p>

    <h3>Value Binding</h3>
    <input type="checkbox" id="valueBinding" v-model="checked" true-value="Anto" false-value="Ruto">
    <label for="valueBind">{{ checked }}</label>
    
    <h2>Modifiers</h2>
    <h3>Lazy Modifier</h3>
    <input v-model.lazy="lazyModifier" />
    <p>Lazy Modifier: {{ lazyModifier }}</p>

    <h3>Number Modifier</h3>
    <input v-model.number="numberModifier" />
    <p>Number Modifier: {{ numberModifier }}</p>
    
</template>