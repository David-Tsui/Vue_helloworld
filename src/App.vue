<template>
	<div id="fullpage">
		<!-- <img class="logo" src="./assets/logo.png"> -->
		<First></First>
		<Second></Second>
		<Third></Third>
	</div>
</template>

<script>
import First from './components/First'
import Second from './components/Second'
import Third from './components/Third'

export default {
	components: {
		First,
		Second,
		Third
	}
}
</script>

<style lang="scss">
html {
	height: 100%;
}

body {
	display: flex;
	align-items: center;
	justify-content: center;
	height: 100%;
}

#fullpage {
	color: #2c3e50;
	margin-top: -100px;
	max-width: 600px;
	font-family: Source Sans Pro, Helvetica, sans-serif;
	text-align: center;
	a {
		color: #42b983;
		text-decoration: none;
	}
}

.logo {
	width: 100px;
	height: 100px
}
</style>
