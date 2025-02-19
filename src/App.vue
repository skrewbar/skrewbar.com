<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <RouterLink to="/">홈</RouterLink>
        <!-- TODO -->
        <RouterLink to="/links">링크</RouterLink>
        <RouterLink to="/data">자료</RouterLink>
        <!-- 미구현 -->
        <a href="https://skrewbar.github.io">블로그</a>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
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
  margin-top: 2rem;

  width: 100%;
  height: 10vh;

  justify-content: space-evenly;
}

nav a.router-link-exact-active {
  color: var(--vt-c-black);
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  font-size: 24px;
  flex-grow: 1;

  text-decoration: none;
  color: rgb(136, 136, 136);
  transition: 0.4s;
}

@media (hover: hover) {
  a:hover {
    color: rgb(0, 0, 0);
  }
}
</style>
