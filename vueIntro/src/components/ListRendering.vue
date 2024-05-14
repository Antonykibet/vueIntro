<script setup>
    import {ref, reactive} from 'vue'
    const books = ref(['Atomic Habits', '47 Laws of Power','Subtle Art of ...', 'The Mountain is You'])
    const myObject = reactive({
        title: 'How to do lists in Vue',
        author: 'Jane Doe',
        publishedAt: '2016-04-10'
    })
</script>
<template>
    <h1>List Rendering</h1>
    <h2>Books ive read:</h2>
    <li v-for="(book,index) in books">{{ index }} . {{ book }}</li>
    <h2>V-for for objects</h2>
    <li v-for="(value,key) in myObject">
        {{ key}} : {{ value }}
    </li>
    <h2>V-for in a Range</h2>
    <li v-for="n in 5">{{ n }}</li>
</template>