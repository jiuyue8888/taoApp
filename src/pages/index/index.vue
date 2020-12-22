<template>
	<div class="mian">
		<svg-icon icon-class="bg" size="100%,11rem"/>
	</div>
</template>

<script>
	export default {
		name: 'HelloWorld',
		data() {
			return {
				msg: 'Welcome to Your Vue.js App'
			}
		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	.mian {
		position: relative;
		width: 100%;
		height: 100vh;
		background: #2C3E50;
	}
</style>
