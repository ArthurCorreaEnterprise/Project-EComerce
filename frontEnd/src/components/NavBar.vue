<template>
    <div class="navbar-container">
        <div class="logo-section">
            <img alt="Vue logo" src="@/assets/logo.svg" width="125" height="125" />
            <span>SoFi</span>
        </div>
        <nav class="navigation-links">
            <RouterLink class="nav-link" active-class="active" to="/">Home</RouterLink>
            <RouterLink class="nav-link" active-class="active" to="/about">About</RouterLink>
            <RouterLink class="nav-link" active-class="active" to="/store">Store</RouterLink>
            <RouterLink class="nav-link" active-class="active" to="/blog">Blog</RouterLink>
            <RouterLink class="nav-link" active-class="active" to="/sale">Sale</RouterLink>
        </nav>
        <div class="icon-buttons">
            <button type="button">
                <font-awesome-icon :icon="['far', 'heart']" />
            </button>
            <button type="button">
                <font-awesome-icon :icon="['fas', 'cart-shopping']" />
            </button>
            <button type="button" class="user-button">
                <font-awesome-icon :icon="['far', 'user']" />
            </button>
        </div>
    </div>
</template>

<script setup>
import { RouterLink } from 'vue-router'
</script>

<style scoped>
.navbar-container {
    @apply flex justify-between items-center py-2 px-6 bg-white;
}

.logo-section {
    @apply flex justify-between items-center gap-2;
}

.nav-link {
    @apply px-4 py-2 rounded-full text-xs font-semibold text-gray-400;
}

.icon-buttons {
    @apply flex gap-4;
}

.active {
    @apply bg-white text-gray-800;
}

button {
    @apply border flex justify-center items-center size-10 rounded-full;
    @apply hover:border-gray-800 text-gray-800;
}

button.user-button {
    @apply bg-emerald-200;
}

.navigation-links {
    @apply flex justify-between items-center gap-4 py-2 px-4 rounded-full bg-gray-100;
}

img {
    @apply size-10;
}

span {
    @apply font-dancing-script text-3xl font-bold text-emerald-500;
}
</style>
