<template>
	<div class="about-window">
    <Window header="About" :enableBack="true">
			<p>Seinfeld Multiverse is a project where I aim to collect all the movies (and TV shows eventually) where Seinfeld actors and actresses worked together.</p>
			<img src="~assets/kramer.gif" alt="A gif that shows Kramer, from Seinfeld, shaking" />
		</Window>
	</div>
</template>

<script>
export default {
  name: 'About',
	components: ['Window'],
}
</script>

<style>
.about-window img {
  display: block;
  margin: 0 auto;
}
</style>


