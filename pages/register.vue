<template>
    <div class="register-container">
        <h1>Register</h1>
        <NuxtLink to="/" class="home-link">HOME</NuxtLink>
        <br>
        <div class="input-container">
            <label for="email">Email</label>
            <input type="text" name="email" v-model="register.email">
        </div>
        <div class="input-container">
            <label for="username">Username</label>
            <input type="text" name="username" v-model="register.username">
        </div>
        <div class="input-container">
            <label for="password">Password</label>
            <input type="password" name="password" v-model="register.password">
        </div>
        <div class="input-container">
            <button @click="submitRegister">Register</button>
        </div>
        <p class="login-link">
            Already have an account? <NuxtLink to="/login">Login</NuxtLink>
        </p>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import { useRouter } from 'vue-router';

interface Register {
    email: string;
    username: string;
    password: string;
}

const register = ref<Register>(
    {
        email: 'jan@gmail.com',
        username: 'jan',
        password: '12345'
    }
)

const router = useRouter();

const submitRegister = () => {
    // Simulate login logic
    if (register.value.email === 'jan@gmail.com' && register.value.username === 'jan' && register.value.password === '12345') {
        alert('Register successful!');
        router.push('/dashboard');
    } else {
        alert('Invalid email, username or password');
    }
}
</script>

<style lang="scss" scoped>
.register-container {
    max-width: 400px;
    margin: 0 auto;
    text-align: center;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
    background-color: #f9f9f9;
}

h1 {
    font-size: 24px;
    margin-bottom: 20px;
}

.input-container {
    margin-bottom: 20px;
}

label {
    display: block;
    margin-bottom: 5px;
}

input {
    width: 100%;
    padding: 10px;
    border-radius: 5px;
    border: 1px solid #ccc;
    box-sizing: border-box;
}

button {
    padding: 10px 20px;
    background-color: #008080;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color: #00ffff;
}

.login-link {
    margin-top: 20px;
}
</style>