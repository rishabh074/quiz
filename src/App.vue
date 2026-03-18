<template>
  <div class="ctr">
    <questions v-if="questionsAnswered < questionsData.length" :questionsData="questionsData" :questionsAnswered="questionsAnswered" @question-answered="questionAnswered"/>
    <results v-else :resultsData="resultsData" :totalCorrect="totalCorrect"/>

    <button type="button" class="reset-btn" @click="resetQuiz" v-if="questionsAnswered === questionsData.length">
  Reset
</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import questions from './components/questions.vue'
import results from './components/results.vue'

const questionsAnswered = ref(0)
const totalCorrect = ref(0)

const questionAnswered = (is_correct) => {
  if (is_correct) {
    totalCorrect.value++
  }
  questionsAnswered.value++
}

const questionsData = [
  {
    q: 'What is 2 + 2?',
    answers: [
      { text: '4', is_correct: true },
      { text: '3', is_correct: false },
      { text: 'Fish', is_correct: false },
      { text: '5', is_correct: false }
    ]
  },
  {
    q: 'How many letters are in the word "Banana"?',
    answers: [
      { text: '5', is_correct: false },
      { text: '7', is_correct: false },
      { text: '6', is_correct: true },
      { text: '12', is_correct: false }
    ]
  },
  {
    q: 'Find the missing letter: C_ke',
    answers: [
      { text: 'e', is_correct: false },
      { text: 'a', is_correct: true },
      { text: 'i', is_correct: false }
    ]
  }
]

const resultsData = [
  {
    min: 0,
    max: 2,
    title: "Try again!",
    desc: "Do a little more studying and you may succeed!"
  },
  {
    min: 3,
    max: 3,
    title: "Wow, you're a genius!",
    desc: "Studying has definitely paid off for you!"
  }
]

const resetQuiz = () => {
  questionsAnswered.value = 0
  totalCorrect.value = 0
}
</script>

<style scoped>
</style>