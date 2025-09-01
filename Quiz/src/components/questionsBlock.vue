<template>
    <div v-for="questions in questionsList" key="question"> 
        <li> {{ questions }}</li>
    </div>
</template>

<script setup>
import { ref, onMounted} from 'vue'
import questions from '../assets/questions.json'

const quizData = ref(null)
const questionsList = ref(null)

onMounted( () => {
    quizData.value = questions
    questionsList.value = quizData.value.questions
})

</script>