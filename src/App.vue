<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <RouterLink to="/"><span>홈</span></RouterLink>
        <RouterLink to="/links"><span>링크</span></RouterLink>
        <RouterLink to="/data"><span>자료</span></RouterLink>
        <a href="https://blog.skrewbar.com"><span>블로그</span></a>
        <RouterLink to="/about"><span>About</span></RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />

  <svg id="sunmoon" width="200" height="200">
    <defs>
      <mask id="hole">
        <rect width="100%" height="100%" fill="white" />
        <circle id="overlay" r="80" cx="230" cy="-30" fill="black" />
      </mask>

      <filter id="blur">
        <feDropShadow dx="0" dy="0" stdDeviation="10" flood-color="gold" />
      </filter>
    </defs>

    <g filter="url(#blur)">
      <circle fill="gold" id="donut" r="80" cx="100" cy="100" mask="url(#hole)" />
    </g>
  </svg>
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
  font-size: 1.5rem;
  flex-grow: 1;

  text-decoration: none;
  color: var(--color-text-secondary);
  transition: 0.4s;
}

@media (hover: hover) {
  a:hover {
    color: rgb(0, 0, 0);
  }
}

#sunmoon {
  position: fixed;
  bottom: 3vh;
  right: 1vw;

  border-radius: 50%;
}
</style>
