<template>
    <div class="login-container">
        <h1>Login</h1>
            <NuxtLink to="/">HOME</NuxtLink><br>
        <div class="input-container">
            <label for ="">username</label>
            <input type="text" name="username" v-model="login.username"><br>
        </div>
        <div class="input-container">
            <label for ="">password</label>
            <input type="password" name="password" v-model="login.password"><br>
        </div>
    

        {{ login.username }}<br>
        {{ login.password }}<br>

        <div class="input-container">
            <button @click="submitLogin">Login</button><br>
        </div>
        <p class="register-link">
            Don't have an account? <NuxtLink to="/register">Register</NuxtLink>
        </p>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import { useRouter } from 'vue-router';

interface Login {
    username: string;
    password: string;
}

const login = ref<Login>(
    {
        username: 'jan',
        password: '12345'
    }
)

const router = useRouter();

const submitLogin = () => {
    // Simulate login logic
    if (login.value.username === 'jan' && login.value.password === '12345') {
        alert('Login successful!');
        router.push('/dashboard');
    } else {
        alert('Invalid username or password');
    }
}
</script>

<style lang="scss" scoped>
.login-container {
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

.register-link {
    margin-top: 20px;
}
</style>