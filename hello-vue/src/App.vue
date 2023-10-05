<script setup lang="ts">
import { computed, reactive } from 'vue'

const data = reactive({
  radius: Math.round(Math.random() * 10),
  PI: 3.14
})
const area = computed(() => data.radius * data.radius * data.PI)

setInterval(() => {
  data.radius = Math.round(Math.random() * 10)
}, 1000)
</script>

<template>
  <div>
    <p>半径{{ data.radius }}の円の面積を円周率{{ data.PI }}で計算すると{{ area }}</p>
  </div>
</template>
