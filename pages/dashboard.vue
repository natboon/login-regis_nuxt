<template>
    <div class="dashboard-container">
        <h1>Dashboard</h1>
        <p>Welcome to the dashboard</p>
        <NuxtLink to="/" class="logout-link">Logout</NuxtLink>
    </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.dashboard-container {
    max-width: 600px;
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

.logout-link {
    display: inline-block;
    padding: 10px 20px;
    background-color: #008080;
    color: white;
    border-radius: 5px;
    text-decoration: none;
    transition: background-color 0.3s ease;
}

.logout-link:hover {
    background-color: #00ffff;
}
</style>