<script setup>
// -- Définition des 'props'
const props = defineProps({
  firstName: String,
  firstHobbie: String,
  secondHobbie: String
})
</script>

<template>
  <p>Outside of work, {{ firstName }} likes to {{ firstHobbie }} and {{ secondHobbie }}.</p>
</template>
