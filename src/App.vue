<script setup>
import CardDescription from './components/CardDescription.vue'

const personsList = [
  {
    gender: 'female',
    firstname: 'Emily',
    lastname: 'Parker',
    age: 24,
    job: 'teacher',
    hobbies: ['read books', 'go hiking'],
    pet: {
      name: 'Whiskers',
      age: 2,
      species: 'ferret'
    },
    favoriteColor: 'red'
  },
  {
    gender: 'male',
    firstname: 'Marcus',
    lastname: 'Bennett',
    age: 38,
    job: 'architect',
    hobbies: ['watch bird', 'play chess'],
    pet: {
      name: 'Nala',
      age: 6,
      species: 'dog'
    },
    favoriteColor: 'blue'
  },
  {
    gender: 'female',
    firstname: 'Sophia',
    lastname: 'Rodriguez',
    age: 31,
    job: 'environmental scientist',
    hobbies: ['play guitar', 'bake cakes'],
    pet: {
      name: 'Paws',
      age: 3,
      species: 'cat'
    },
    favoriteColor: 'orange'
  },
  {
    gender: 'male',
    firstname: 'Oliver',
    lastname: 'Hughes',
    age: 56,
    job: 'carpenter',
    hobbies: ['paint', 'ride horses'],
    pet: {
      name: 'Bubble',
      age: 4,
      species: 'snake'
    },
    favoriteColor: 'purple'
  }
]
</script>
<template>
  <main>
    <h1>Description list</h1>
    <div>
      <div><CardDescription :personInfos="personsList[0]" /></div>
      <div><CardDescription :personInfos="personsList[1]" /></div>
      <div><CardDescription :personInfos="personsList[2]" /></div>
      <div><CardDescription :personInfos="personsList[3]" /></div>
    </div>
  </main>
</template>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #c9e1c2;
  height: 100vh;
  padding: 50px;
}
main > div {
  display: flex;
  align-items: center;
  flex: 1;
  gap: 20px;
}
</style>
