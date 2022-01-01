<template>
  <div class="default-layout">
		<header class="layout-header">
			<h1>Seinfeld Multiverse</h1>
			<h2>The web about <s>nothing</s> Seinfeld characters in alternate realities</h2>
		</header>
		<main>
			<Nuxt class="page-content"/>
			<footer>
				<p>
					<NuxtLink class="about-link" to="/about">About</NuxtLink>
				</p>
				<p>
					<img src="~assets/seinfeld-faces.GIF" alt="A gif that shows the faces of the main cast of Seinfeld" />
				</p>
				<p class="footer-message">Made with love and yada yada yada</p>
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

.layout-header {
	margin-bottom: 20px;
	padding: 0.5em;
}

main {
	background-image: url(~/assets/bg.png);
}

.page-content {
	margin-bottom: 30px;
}

h1 {
  text-align: center;
	color: #e80000;
	text-shadow: 2px 2px black;
	font-family: 'Oranienbaum';
	font-size: 3em;
	margin: 0;
	padding: 0.3em;
}

h2 {
	font-size: 1em;
	text-align: center;
	margin: 0;
}

.about-link {
  background: white;
}

footer {
	text-align: center;
	color: white;
}

.footer-message {
	text-shadow: 1px 1px black;
}
</style>

