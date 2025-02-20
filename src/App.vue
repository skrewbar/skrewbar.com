<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
      <nav>
        <RouterLink to="/"><span>홈</span></RouterLink>
        <RouterLink to="/links"><span>링크</span></RouterLink>
        <RouterLink to="/data"><span>자료</span></RouterLink>
        <a href="https://blog.skrewbar.com"><span>블로그</span></a>
        <RouterLink to="/about"><span>About</span></RouterLink>
      </nav>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

nav {
  display: flex;
  font-size: 12px;
  text-align: center;

  width: 100%;
  height: 10vh;

  justify-content: space-evenly;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a {
  display: flex;
  align-items: center;
  padding: 0 1rem;
  font-size: 1.75rem;
  flex-grow: 1;

  text-decoration: none;
  color: var(--color-text-secondary);
  transition: 0.4s;
}

@media (hover: hover) {
  a:hover {
    color: var(--color-text);
  }
}
</style>
