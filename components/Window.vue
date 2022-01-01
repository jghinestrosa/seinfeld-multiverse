<template>
	<section class="window-container">
		<header>
			<NuxtLink class="backButton" v-if="enableBack" to="/">X</NuxtLink>
			<h3><span>{{header}}</span></h3>
		</header>
		<div class="window-content">
			<slot></slot>
		</div>
	</section>
</template>

<script>
export default {
  props: ['enableBack', 'header'],
};
</script>

<style>
section.window-container h3 {
  text-align: center;
	border-bottom: 2px solid black;
	margin: 0;
	padding: 5px;
	background: lightgray;
}

section.window-container h3 span {
	background: white;
	padding-left: 10px;
	padding-right: 10px;
}

section.window-container {
	position: relative;
  border: 2px solid black;
	max-width: 90vw;
	margin: 0 auto;
  box-shadow: 3px 3px black;
	background: white;
	font-family: 'VT323', monospace;
	/*font-family: monospace;*/
  /*font-size: 16px;*/
  font-size: 1.5em;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
}

section.window-container .backButton {
	/*content: 'X';*/
	position: absolute;
	top: 3px;
	left: 3px;
	text-decoration: none;
	color: black;
	padding-left: 3px;
	padding-right: 3px;
	border: 2px solid black;
	background: white;
}

section.window-container .backButton:hover {
	background: darkgray;
}

section.window-container .backButton:active {
	background: lightgray;
}

section.window-container .window-content {
  padding: 0.5em; /* with vt323... with monospace maybe 1em*/
}

@media (min-width: 800px) {
	section.window-container {
		max-width: 80vw;
	}
}
</style>
