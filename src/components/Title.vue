<script setup>
// -- Définition des 'props'
const props = defineProps({
  firstName: String,
  lastName: String
})
</script>

<template>
  <h2>{{ firstName }} {{ lastName }}</h2>
</template>
