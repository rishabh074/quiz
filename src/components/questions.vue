<template>
    <div>

        <div class="questions-ctr">
        <div class="progress">
            <div class="bar" :style="{ width: progressPercent + '%' }"></div>
            <div class="status">{{ questionsAnswered }} out of {{ questionsData.length }} questions answered</div>
        </div>
        <div class="single-question" v-for="(question, qi) in questionsData" :key="question.q" v-show="questionsAnswered===qi">
            <div class="question">{{ question.q }}</div>
            <div class="answers">
                <div class="answer" v-for="answer in question.answers" :key="question.answers" @click.prevent="selectAnswer(answer.is_correct)" >
                    {{ answer.text }}
                </div>
                
            </div>
        </div>
    </div>

    </div>
</template>

<script setup>
import { computed } from 'vue'


const props = defineProps({
  questionsData: {
    type: Array,
    required: true
  },
  questionsAnswered: {
    type: Number,
    required: true
  }
})

const emit = defineEmits(['question-answered'])

const selectAnswer = (isCorrect) => {
  emit('question-answered', isCorrect)
}
const progressPercent = computed(() => {
  return (props.questionsAnswered / props.questionsData.length) * 100
})

</script>

<style lang="scss" scoped>

</style>