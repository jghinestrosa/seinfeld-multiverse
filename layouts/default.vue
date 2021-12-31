<template>
  <div class="default-layout">
		<header>
			<h1>Seinfeld Multiverse</h1>
			<h2>The web about <s>nothing</s> Seinfeld characters in alternative realities</h2>
		</header>
		<main>
			<Nuxt class="hola"/>
			<footer>
				<img src="~assets/seinfeld-faces.GIF" alt="A gif that shows the faces of the main cast of Seinfeld" />
				<p>Made with love and yada yada yada</p>
			</footer>
		</main>
  </div>
</template>

<script>

export default {};
</script>

<style>
html {
  box-sizing: border-box;
}

header {
	/*padding: 1em;*/
	min-height: 22vh;
}

main {
	min-height: 77vh;
	background-image: url(~/assets/bg.png);
}

.hola {
	min-height: 55vh;
}

h1 {
  text-align: center;
	color: #e80000;
	text-shadow: 2px 2px black;
	font-family: 'Oranienbaum';
	font-size: 3em;
	/*margin: 0.3em 0;*/
	margin: 0;
	padding: 0.3em;
}

h2 {
	font-size: 1em;
	text-align: center;
	margin: 0;
}

footer {
	text-align: center;
	min-height: 5vh;
	color: white;
	/*padding: 1.5em;*/
}
</style>

