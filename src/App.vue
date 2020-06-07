<template>
	<div id="app">
		<div class="container">
			<img alt="Vue logo" src="./assets/logo.png" />
			<hr />
			<div class="row">
				<div class="col-12 mb-3">
					<h3 class="font-weight-bold text-uppercase">
						Planes para cursos en programacion Vue.js
					</h3>
					<small class="text-muted"
						>Haz click en los botones para aumentar la cantidad</small
					>
				</div>
			</div>
      <Planes />
		</div>
	</div>
</template>

<script>
	import Planes from './components/Planes'

	export default {
		name: 'App',
		components: {
			Planes,
		}
	}
</script>

<style>
	#app {
		font-family: Avenir, Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
		color: #2c3e50;
		margin-top: 60px;
	}
</style>
