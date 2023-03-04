<template>
	<NavbarComp />
	<WelcomeComp />
</template>

<script>
	import "../styles/global.css";
	import NavbarComp from "./components/NavbarComp.vue";
	import WelcomeComp from "./components/WelcomeComp.vue";

	export default {
		name: "App",
		components: {
			NavbarComp,
			WelcomeComp,
		},
	};
</script>

<style>
	h1 {
		border-bottom: #2c3e50 1px solid;
		display: inline-block;
		padding-bottom: 2px;
	}
</style>
