<script setup>
// -- Définition des 'props'
const props = defineProps({
  gender: String,
  petName: String,
  petAge: Number,
  petSpecies: String
})
// console.log(props.gender)
// console.log(props.petName)
// console.log(props.petAge)
// console.log(props.petSpecies)
</script>

<template>
  <p>
    At home, {{ gender === 'female' ? 'her' : 'his' }} lively companion is {{ petName }} a
    {{ petAge }}-year_old {{ petSpecies }}.
  </p>
</template>
