<script setup>
import { ref, computed } from 'vue'
const reviews = ref(googleReviewsData.count)
const average = computed(() => {
  return googleReviewsData.averageScore.toFixed(1);
})

const getLang = computed(() => {
  return document.querySelector('html').getAttribute('lang')
})

</script>

<template>
  <div>
    <div>
      <p>{{ average }} of 5.0</p>
      <p>{{ reviews }} Customer ratings</p>
    </div>
  </div>
</template>