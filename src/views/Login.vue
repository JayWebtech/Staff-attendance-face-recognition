<template>
	<div class="login-container">
		<div class="login-card">
			<img src="../assets/logox.png"  class="image">
			<h1 class="login-title">Admin Login</h1>
			<div class="login-form">
				<label for="username" class="login-label">Username:</label>
				<input type="text" id="username" v-model="username" class="login-input" />
				<label for="password" class="login-label">Password:</label>
				<input type="password" id="password" v-model="password" class="login-input" />
				<button class="login-button" @click="login">Login</button>
				<p v-if="error" class="login-error">{{ error }}</p>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			username: '',
			password: '',
			error: ''
		};
	},
	methods: {
		login() {
			if (this.username === 'admin' && this.password === 'admin') {
				// Correct credentials, navigate to the next page
				this.$router.push('/Admin');
			} else {
				// Incorrect credentials, display error message
				this.error = 'Invalid username or password';
			}
		}
	}
};
</script>

<style scoped>
.login-container {
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
background-color: #FAEBD7;
}
.image{
width: 150px;
height: 150px;
margin: 0 auto;
}
.login-card {
background-color: #fff;
padding: 40px;
border-radius: 5px;
box-shadow: 0 2px 6px rgba(0, 0, 0, 0.2);
max-width: 600px;
width: 100%;
}

.login-title {
text-align: center;
font-size: 24px;
margin-bottom: 20px;
}

.login-form {
display: flex;
flex-direction: column;
}

.login-label {
margin-bottom: 5px;
text-align: left !important;
}

.login-input {
padding: 10px;
border-radius: 3px;
border: 1px solid #ccc;
margin-bottom: 10px;
}

.login-button {
padding: 10px;
background-color: #4F46E5;
color: #fff;
border: none;
border-radius: 3px;
cursor: pointer;
}

.login-error {
color: red;
margin-top: 10px;
}
</style>
