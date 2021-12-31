<template>
	<div class="character">
		<h5>{{character.inSeinfeld.name}} is {{character.inMovie.name}}</h5>
		<div class="character-data">
			<CharacterImg id="character-in-movie" :imgSrc="character.inMovie.img"/>
			<p class="character-description">{{character.description}}</p>
			<CharacterImg id="character-in-seinfeld" :imgSrc="character.inSeinfeld.img"/>
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
	grid-template-columns: repeat(2, 1fr);
	grid-template-rows: 1fr;
	grid-gap: 10px;
	justify-content: center;
	margin-bottom: 20px;
}

#character-in-movie {
	grid-column: 1;
	grid-row: 1;
}

#character-in-seinfeld {
	grid-column: 2;
	grid-row: 1;
}

.character-description {
	grid-column: 1 / 3;
	grid-row: 2;
}

.character-data p {
	margin: 0;
	text-align: center;
}

@media (min-width: 800px) {
	.character-data {
		/*grid-template-columns: 250px auto 250px;*/
		grid-template-columns: repeat(3, 1fr);
		grid-template-rows: 1fr;
	}

	#character-in-movie {
		grid-column: 1;
	}

	#character-in-seinfeld {
		grid-column: 3;
	}

	.character-description {
		grid-column: 2;
		grid-row: 1;
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

