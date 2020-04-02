<template>
	<header>
		<button v-on:click="changeTitle">Thay đổi text header ở components con</button>
		<h1>{{ sayHello + ' ' + text }}</h1>
	</header>
</template>

<script>
	export default {
		name: 'header-component',
		data() {
			return {
				text: 'Header'
			}
		},
		props: {
			sayHello: {
				type: String,
				default: 'Hihi'
			}
		},
		methods: {
			changeTitle() {
				this.$emit('handleTitleEvent', { sayHello: 'Hi !' });
			}
		}
	}
</script>

<style>
	
</style>