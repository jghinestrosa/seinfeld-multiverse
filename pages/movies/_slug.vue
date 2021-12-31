<template>
	<div>
    <Window :header="movie.title" :enableBack="true">
			<MovieDetail :movie="movie" />
		</Window>
	</div>
</template>

<script>
export default {
  name: 'MoviePage',
	components: ['Window'],
  async asyncData({ $content, params }) {
    const movie = await $content('movies', params.slug).fetch();
    return { movie };
  }
}
</script>

<style>
</style>

