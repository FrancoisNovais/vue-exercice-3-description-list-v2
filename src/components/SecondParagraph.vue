<script setup>
// -- Définition des 'props'
const props = defineProps({
  firstName: String,
  firstHobbie: String,
  secondHobbie: String
})
// console.log(props.firstName)
// console.log(props.firstHobbie)
// console.log(props.secondHobbie)
</script>

<template>
  <p>Outside of work, {{ firstName }} likes to {{ firstHobbie }} and {{ secondHobbie }}.</p>
</template>
