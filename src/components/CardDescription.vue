<script setup>
import Title from './Title.vue'
import FirstParagraph from './FirstParagraph.vue'
import SecondParagraph from './SecondParagraph.vue'
import ThirdParagraph from './ThirdParagraph.vue'

// -- Définition des 'props'
const props = defineProps({
  personInfos: Object
})
// console.log(props.personInfos)
</script>

<template>
  <section>
    <img
      src="https://res.cloudinary.com/lereacteur-apollo/image/upload/v1704967000/RNCP31114/cours-vue/exo-sem-1/mystery-person_bueack.jpg"
      alt="photo de profil"
    />

    <div>
      <Title
        :class="personInfos.gender"
        :firstName="personInfos.firstname"
        :lastName="personInfos.lastname"
      />
      <FirstParagraph :gender="personInfos.gender" :age="personInfos.age" :job="personInfos.job" />
      <SecondParagraph
        :firstName="personInfos.firstname"
        :firstHobbie="personInfos.hobbies[0]"
        :secondHobbie="personInfos.hobbies[1]"
      />
      <ThirdParagraph
        :gender="personInfos.gender"
        :petName="personInfos.pet.name"
        :petAge="personInfos.pet.age"
        :petSpecies="personInfos.pet.species"
      />
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
  box-shadow: 0 0 7px v-bind(personInfos.favoriteColor);
}
section > div {
  flex: 1;
}
img {
  width: 100%;
  object-fit: cover;
  object-position: top;
  border-radius: 5px;
}

svg {
  align-self: flex-end;
  font-size: 26px;
  color: grey;
  cursor: pointer;
}
svg:hover {
  color: #000000;
}
h2 {
  font-weight: bold;
  margin: 20px 0 10px 0;
  font-size: 18px;
}
.female {
  color: orange;
}
p {
  line-height: 18px;
  padding-bottom: 5px;
}
</style>
