<template>
	<div class="navbar">
		<div class="nav-items">
			<div class="nav-item" v-for="item in navbarItems" :key="item.id">
				<h3>
					<a :href="item.href">
						{{ item.text }}
					</a>
				</h3>
			</div>
		</div>
		<AuthComp />
	</div>
</template>

<script>
	import AuthComp from "./AuthComp.vue";

	export default {
		data() {
			return {
				navbarItems: [
					{
						id: 1,
						text: "Home",
						href: "/",
					},
					{
						id: 2,
						text: "Profile",
						href: "/profile",
					},
				],
			};
		},
		components: { AuthComp },
	};
</script>

<style>
	.navbar {
		position: relative;
		background-color: #2e429b;
		height: 40px;
		width: 100%;
		display: flex;
		justify-content: space-between;
	}

	.nav-items {
		display: flex;
		gap: 50px;
		margin-left: 25px;
	}

	.nav-item {
		height: 100%;
		color: #cfd8ff;
		display: flex;
		align-items: center;
	}

	.navbar a {
		text-decoration: none;
		color: #cfd8ff;
	}
	.navbar a:hover {
		color: #f5f7ff;
	}
</style>
