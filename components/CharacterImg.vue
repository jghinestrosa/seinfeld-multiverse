<template>
	<img :src="require(`~/assets/${imgSrc2}`)" alt="" class="character-image" width="250" height="250"></img>
</template>

<script>
export default {
  props: ['imgSrc'],
  computed: {
		imgSrc2() {
			return this.imgSrc ? this.imgSrc : 'unknown-character.jpg';
		}
	}
};
</script>

<style>
.character-image {
  border: 2px solid black;
	max-width: 95%;
	width: 150px;
	height: auto;
	margin: 0 auto;
	background: lightgray;
}

@media (min-width: 800px) {
	.character-image {
		width: auto;
	}
}
</style>

