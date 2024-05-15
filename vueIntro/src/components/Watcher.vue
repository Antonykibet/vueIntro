<script setup>
    import {ref, watch} from 'vue'
    
    const question = ref('A question should include a question mark...')
    const answer = ref('')
    const disabled = ref(false)
    
    watch(question,async(newQuestion,oldQuestion)=>{
        try {
            if (newQuestion.includes('?')) {
                console.log('Hitt');
                let response = await fetch('https://yesno.wtf/api')
                let result = await response.json()
                answer.value = result.answer
            }
        } catch (error) {
            answer.value = 'Error getting API results' + error   
        }
    })
</script>
<template>
    <h1>Watcher</h1>
    <input type="text" v-model="question" :disabled="disabled">
    <p>Answer: {{ answer }}</p>
    <i>NB:You can use watchEffect if you dont want to specify the dependancies</i>
</template>