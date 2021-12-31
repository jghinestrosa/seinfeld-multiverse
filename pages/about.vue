<template>
	<div class="about-window">
    <Window header="About" :enableBack="true">
			<img src="~assets/seinfeld.gif" alt="A gif that shows the Seinfeld TV show logo" />
			<h4>What is this?</h4>
			<p>Seinfeld Multiverse is a project where I aim to collect all the movies where Seinfeld actors and actresses worked together.</p>
			<h4>Why?</h4>
			<p>I've been rewatching some 90s movies recently and I was truly surprised when I started to spot actors and actresses from Seinfeld on them really often. Even four or five in the same movie! This made me look at the movies as parallel universes to the Seinfeld one, where same people from Seinfeld exists but they are totally different.</p>
			<h4>Any restriction?</h4>
			<p>This project DOES NOT include those movies where only one single actor or actress from Seinfeld appears. At least two actors or actresses should play a role in the same movie. It doesn't matter if they don't interact between them.</p>
			<h4>I want to collaborate!</h4>
			<p>TBD</p>
			<p>Have fun and giddy up!</p>
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

.about-window h4 {
	margin: 0.5em 0; /* think about moving h4 and h5 rules inside windows to the Window component... */
}
</style>


