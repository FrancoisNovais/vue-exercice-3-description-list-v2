<script setup>
// -- Définition des 'props'
const props = defineProps({
  gender: String,
  petName: String,
  petAge: Number,
  petSpecies: String
})
</script>

<template>
  <p>
    At home, {{ gender === 'female' ? 'her' : 'his' }} lively companion is {{ petName }} a
    {{ petAge }}-year_old {{ petSpecies }}.
  </p>
</template>
