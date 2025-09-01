<template>
  <div>
    <h1 class="text-3xl"> {{ title }}</h1>
    <p ></p>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import questions from '../assets/questions.json'

const quizData = ref(null)
const title = ref('')

onMounted(() => {
  quizData.value = questions
  title.value = quizData.value.title
})

</script>