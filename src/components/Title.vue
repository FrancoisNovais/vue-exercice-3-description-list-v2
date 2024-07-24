<script setup>
// -- Définition des 'props'
const props = defineProps({
  firstName: String,
  lastName: String
})
// console.log(props.firstName)
// console.log(props.lastName)
</script>

<template>
  <h2>{{ firstName }} {{ lastName }}</h2>
</template>
