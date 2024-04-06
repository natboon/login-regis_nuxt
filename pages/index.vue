<template>
    <div class="home">
        <h1>Home page</h1>
    </div>
    <div class="buttons">
        <NuxtLink to="/login" class="login-button">LOGIN</NuxtLink> <br>
        <NuxtLink to="/register" class="register-button">REGISTER</NuxtLink>
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.home {
  text-align: center;
}

h1 {
  font-size: 34px;
  margin-bottom: 30px;
}

.buttons {
  margin-top: 50px;
  display: flex;
  justify-content: center;
}

.login-button,
.register-button {
  padding: 10px 20px;
  margin: 50px;
  background-color: #008080;
  color: white;
  text-decoration: none;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

.login-button:hover,
.register-button:hover {
  background-color: #00FFFF;
}
</style>