<template>
	<img :src="require(`~/assets/${imgSrc2}`)" alt="" class="character-image"></img>
</template>

<script>
export default {
  props: ['imgSrc'],
  computed: {
		imgSrc2() {
			return this.imgSrc ? this.imgSrc : 'unknown.jpg';
		}
	}
};
</script>

<style>
.character-image {
  border: 2px solid black;
	max-width: 95%;
	width: 150px;
	margin: 0 auto;
}

@media (min-width: 800px) {
	.character-image {
		width: auto;
	}
}
</style>

