<script setup>
    import DynamicProps from './DynamicPropPassing.vue'
    import {ref} from 'vue'
    defineProps(['title','blogTitle'])
    const posts = ref([
    { id: 1, title: 'My journey with Vue' },
    { id: 2, title: 'Blogging with Vue' },
    { id: 3, title: 'Why Vue is so fun' }
  ])
</script>
<template>
    <h1>Components Basics</h1>
    <h2>Passing Props</h2>
    <h3>Blog Example</h3>
    <div class="BlogPost">
        <h4>{{ title }}</h4>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Natus inventore nemo aut tempora eum. Quos reiciendis alias corrupti iure ducimus soluta rerum minima, officia quisquam, culpa quam eaque accusamus tenetur?</p>
    </div>
    <h3>Blog Example(Dynamic)</h3>
    <DynamicProps 
        v-for="post in posts"
        :key="post.id"
        :blogTitle="post.title"
    />
</template>
<style scoped>
div{
    border: solid;
    margin-bottom: 8px;
}
</style>