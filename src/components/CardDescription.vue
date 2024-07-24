<script setup>
import Title from './Title.vue'
import FirstParagraph from './FirstParagraph.vue'
import SecondParagraph from './SecondParagraph.vue'
import ThirdParagraph from './ThirdParagraph.vue'
</script>

<template>
  <section>
    <img
      src="https://res.cloudinary.com/lereacteur-apollo/image/upload/v1704967000/RNCP31114/cours-vue/exo-sem-1/mystery-person_bueack.jpg"
      alt="photo de profil"
    />

    <div>
      <Title />
      <FirstParagraph />
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
p {
  line-height: 20px;
  margin: 5px 0;
}
svg {
  /* Permet au coeur d'avoir un alignement différent des autres éléments */
  align-self: flex-end;
  font-size: 26px;
  color: grey;
  cursor: pointer;
}
</style>
