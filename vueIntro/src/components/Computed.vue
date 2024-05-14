<script setup>
    import { ref, reactive, computed } from 'vue';
    const author = reactive({
        author:'Anto',
        books: [
            'Vue 2 - Advanced Guide',
            'Vue 3 - Basic Guide',
            'Vue 4 - The Mystery'
        ]
    })
    const hasBooks = computed(()=>{
        return author.books.length > 0 ? 'Has Books' : 'Does not have any books'
    })
</script>
<template>
    <h1>Computed</h1>
    <p>For complex and verbose expressions and also to eliminate repetions, one can use computed(). Instead of: <br></p>
    <h3>{{ author.books.length > 0 ? 'Has Books' : 'Does not have any books' }}</h3>
    <p>One can do this: <br></p>
    <h3>{{ hasBooks }}</h3>
</template>