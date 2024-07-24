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

<style scoped>
h2 {
  font-weight: bold;
  margin: 20px 0 10px 0;
  font-size: 18px;
}
</style>
