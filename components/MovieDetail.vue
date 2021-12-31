<template>
	<div class="movie-detail-wrapper">
		<p>Year: {{movie.year}}</p>
		<div class="character" v-for="character in movie.characters">
			<img class="character-image" :src="require(`~/assets/${character.inMovie.img}`)" alt="" />
      <p>{{character.description}}</p>
		</div>
	</div>
</template>

<script>
export default {
  props: ['movie']
};
</script>

<style>
.movie-detail-wrapper p {
	max-width: 60%;
}

.character {
	display: flex;
	flex-flow: row wrap;
	justify-content: space-around;
	align-items: center;
	margin-bottom: 20px;
}

.character-image {
  border: 1px solid black;
	box-shadow: 1px 1px black;
	max-width: 95%;
	/*margin: 0.5em;*/
}
</style>

