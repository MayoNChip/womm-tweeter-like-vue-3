<template>
	<div class="auth-buttons">
		<button @click="toggleRegisterModal" class="button">Register</button>
		<button @click="toggleLoginModal" class="button">Login</button>
	</div>
	<ModalComp v-if="showRegisterModal" @close="toggleRegisterModal">
		<template v-slot:title>
			<h1>Register</h1>
		</template>
		<template v-slot:body>
			<form>
				<div class="form-data">
					<h3>Email</h3>
					<input type="text" />
					<h3>Password</h3>
					<input type="text" />
					<h3>Confirm Password</h3>
					<input type="text" />
				</div>
				<button class="button">Register</button>
			</form>
		</template>
	</ModalComp>
	<ModalComp v-if="showLoginModal" @close="toggleLoginModal">
		<template v-slot:title>
			<h1>Login</h1>
		</template>
		<template v-slot:body>
			<form>
				<div class="form-data">
					<h3>Email</h3>
					<input type="text" />
					<h3>Password</h3>
					<input type="text" />
				</div>
				<button class="button">Login</button>
			</form>
		</template>
	</ModalComp>
</template>

<script>
	import ModalComp from "./ModalComp.vue";
	export default {
		components: {
			ModalComp,
		},
		data() {
			return {
				showLoginModal: false,
				showRegisterModal: false,
			};
		},
		methods: {
			handleClick() {
				console.log(this.$refs.name);
				this.$refs.name.classList.add("active");
				this.$refs.name.focus();
			},
			toggleRegisterModal() {
				this.showRegisterModal = !this.showRegisterModal;
			},
			toggleLoginModal() {
				this.showLoginModal = !this.showLoginModal;
			},
		},
	};
</script>

<style>
	.auth-buttons {
		display: flex;
	}
</style>
