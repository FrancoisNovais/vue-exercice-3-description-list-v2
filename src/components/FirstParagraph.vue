<script setup>
// -- Définition des 'props'
const props = defineProps({
  gender: String,
  age: Number,
  job: String
})
// console.log(props.gender)
// console.log(props.age)
// console.log(props.job)
</script>

<template>
  <p>{{ gender === 'female' ? 'She' : 'He' }} is a {{ age }}-year_old {{ job }}.</p>
</template>
