<script>
    export default{
        data(){
            return {
                message:'Woyoo',
                seen:true
            }
        },
        methods: {
            hello(msg){
                alert(msg)
            }
        }
    }
</script>

<template>
    <h2>{{ message }}</h2>
    <button v-on:click="hello('Woyoooo!')">Woyoo button</button>
    <p v-if="seen">You are seeing this message coz i want you to...</p>
</template>

<style></style>