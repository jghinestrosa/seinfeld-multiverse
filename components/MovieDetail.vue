<template>
	<div class="movie-detail-wrapper">
		<p>Year: {{movie.year}}</p>
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
</style>

