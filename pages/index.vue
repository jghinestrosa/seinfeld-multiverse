<template>
	<div>
    <Window header="List of movies">
			<ul>
				<li v-for="item in list">
					<NuxtLink :to="'/movies/' + item.slug">
						{{item.title}}
					</NuxtLink>
				</li>
			</ul>
		</Window>
	</div>
</template>

<script>
export default {
  name: 'IndexPage',
	components: ['Window'],
	async asyncData({ $content, params }) {
    const list = await $content('movies', params.slug)
      .only(['title', 'slug'])
      .sortBy('title', 'asc')
      .fetch();

    return { list };
  }
}
</script>

<style>
</style>
