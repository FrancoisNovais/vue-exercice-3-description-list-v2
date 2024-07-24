<script setup>
import Title from './Title.vue'
import FirstParagraph from './FirstParagraph.vue'
// import SecondParagraph from './SecondParagraph.vue'
// import ThirdParagraph from './ThirdParagraph.vue'

// -- Définition des 'props'
const props = defineProps({
  personInfos: Object
})
</script>

<template>
  <section>
    <img
      src="https://res.cloudinary.com/lereacteur-apollo/image/upload/v1704967000/RNCP31114/cours-vue/exo-sem-1/mystery-person_bueack.jpg"
      alt="photo de profil"
    />

    <div>
      <Title :firstName="personInfos.firstname" :lastName="personInfos.lastname" />
      <FirstParagraph :gender="personInfos.gender" :age="personInfos.age" :job="personInfos.job" />
      <SecondParagraph />
      <ThirdParagraph />
    </div>

    <font-awesome-icon :icon="['fas', 'heart']" />
  </section>
</template>

<style scoped>
section {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  border-radius: 10px;
  padding: 15px;
  height: 500px;
  background-color: #efeeee;
  box-shadow: 0 0 7px grey;
}
section > div {
  flex: 1;
}
img {
  width: 100%;
  /* Détermine la hauteur automatiquement de manière à respecter le ratio donné */
  aspect-ratio: 16/10;
  object-fit: cover;
  object-position: top;
  border-radius: 5px;
}

svg {
  /* Permet au coeur d'avoir un alignement différent des autres éléments */
  align-self: flex-end;
  font-size: 26px;
  color: grey;
  cursor: pointer;
}
h2 {
  font-weight: bold;
  margin: 20px 0 10px 0;
  font-size: 18px;
}
p {
  line-height: 18px;
  padding-bottom: 5px;
}
</style>
