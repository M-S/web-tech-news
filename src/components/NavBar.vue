
<template>
     <nav class="navbar">
        <RouterLink to="/">Home</RouterLink>
      </nav>
</template>
<style scoped>
    .navbar {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 20px;
        border: 2px solid #e0e0e0;
    }
    .navbar a {
        text-decoration: none;
        color: #333;
        font-weight: bold;
    }
    .navbar a:hover {
        color: #000;
    }
    .navbar a.active {
        color: #000;
    }
</style>