<script setup>
// -- Définition des 'props'
const props = defineProps({
  gender: String,
  age: Number,
  job: String
})
</script>

<template>
  <p>{{ gender === 'female' ? 'She' : 'He' }} is a {{ age }}-year_old {{ job }}.</p>
</template>

<style scoped></style>
