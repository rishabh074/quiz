<template>
    <div>

        <div class="result">
        <div class="title">{{ resultsData[resultIndex].title }}</div>
        <div class="desc" {{ resultsData[resultIndex].desc }}>
            Enter a short description here about the result.
        </div>
    </div>

    </div>
</template>

<script setup>

import { computed } from 'vue'



const resultIndex = computed(() => {
  let index = 0

  props.resultsData.forEach((e, i) => {
    if (e.min <= props.totalCorrect && e.max >= props.totalCorrect) {
      index = i
    }
  })

  return index
})


const props = defineProps({
  resultsData: {
    type: Array,
    required: true
  },
  totalCorrect: {
    type: Number,
    required: true
  }
})


</script>

<style lang="scss" scoped>

</style>