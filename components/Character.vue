<template>
	<div class="character">
		<h5>{{character.inSeinfeld.name}} is {{character.inMovie.name}}</h5>
		<div class="character-data">
			<CharacterImg :imgSrc="character.inMovie.img"/>
			<p>{{character.description}}</p>
			<CharacterImg :imgSrc="character.inSeinfeld.img"/>
		</div>
	</div>
</template>

<script>
import CharacterImg from './CharacterImg.vue';

export default {
  props: ['character'],
  components: {
    CharacterImg
  }
};
</script>

<style>
.character h5 {
	font-size: 1.2em;
  text-align: center;
	margin: 1em 0;
	text-decoration: underline;
}

.character-data {
	display: grid;
	grid-template-columns: auto;
	grid-gap: 10px;
	justify-content: center;
	margin-bottom: 20px;
}

.character-data p {
	margin: 0;
	text-align: center;
}

@media (min-width: 800px) {
	.character-data {
		grid-template-columns: 250px auto 250px;
		justify-content: space-between;
	}

	.character-data p {
		margin: 0;
		text-align: left;
	}

	.character h5 {
		font-size: 1.5em;
	}
}
</style>

