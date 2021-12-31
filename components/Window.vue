<template>
	<section>
		<h3><span>{{header}}</span></h3>
		<div class="window-content">
			<slot></slot>
		</div>
	</section>
</template>

<script>
export default {
  props: ['header']
};
</script>

<style>
section h3 {
  text-align: center;
	border-bottom: 2px solid black;
	margin: 0;
	padding: 5px;
	background: lightgray;
}

section h3 span {
	background: white;
	padding-left: 10px;
	padding-right: 10px;
}

section {
	position: relative;
  border: 2px solid black;
	max-width: 80vw;
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

section::before {
	content: 'X';
  position: absolute;
	top: 3px;
	left: 3px;
	padding-left: 3px;
	padding-right: 3px;
	border: 2px solid black;
	background: white;
}

section .window-content {
  padding: 0.5em; /* with vt323... with monospace maybe 1em*/
}
</style>
