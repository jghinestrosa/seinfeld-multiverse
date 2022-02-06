<template>
  <div class="movie-detail-wrapper">
    <div class="movie-metadata">
      <p>Directed by: {{movie.director}}</p>
      <p>Year: {{movie.year}}</p>
    </div>
    <h4>In this universe...</h4>
    <Character v-for="character in movie.characters" :character="character" />
  </div>
</template>

<script>
import CharacterImg from './CharacterImg.vue';
import Character from './Character.vue';

export default {
  props: ['movie'],
  components: {
   CharacterImg
  }
};
</script>

<style>
.movie-detail-wrapper h4 {
  text-align: center;
	margin: 0.5em 0;
}

.movie-detail-wrapper .movie-metadata {
  margin-bottom: 1.3em;
}

.movie-detail-wrapper .movie-metadata p {
  text-align: center;
	margin: 0.5em 0;
}
</style>

