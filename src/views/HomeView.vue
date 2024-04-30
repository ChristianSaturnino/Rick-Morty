<script setup>
import { onMounted, reactive, ref } from 'vue';
import "../assets/home.css"
import ListCharacters from '../components/ListCharacters.vue';

const characters = ref([]);
onMounted(() => {
  fetch("https://rickandmortyapi.com/api/character?limit=50&offset=0")
  .then(response => response.json())
  .then(response => {
    characters.value = response.results;
    console.log(characters);


  });
});

</script>

<template>
  <main>
    <div class="row m-3">
      
  <div class="col-md-6" v-for="character in characters" :key="character.id">
    <div class="card mb-3" style="max-width: 660px;">
      <div class="row g-0">
        <div class="col-md-4">
          <img :src="character.image" height="100%" width="100%" class="card-img-top" alt="...">
        </div>
        <div class="col-md-8">
          <div class="card-body">
            <h5 class="card-title">{{ character.name }}</h5>
            <p class="card-text">Status: {{ character.status }}</p>
            <p class="card-text">Species: {{ character.species }}</p>
            <p class="card-text">Location: {{ character.location.name }}</p>
            <p class="card-text text-white">Episodes: {{ character.episode.length }}</p>
            <p class="card-text "><small class="text-body-white">Gender: {{ character.gender }}</small></p>

          </div>
        </div>
      </div>
    </div>
  </div>
</div>
  
  </main>
</template>
