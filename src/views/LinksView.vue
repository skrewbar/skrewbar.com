<script setup lang="ts">
import { toast } from 'vue3-toastify'
import 'vue3-toastify/dist/index.css'

function copyEmail() {
  navigator.clipboard.writeText('skurua1244@gmail.com')
  toast('이메일이 클립보드에 복사되었습니다!', {
    theme: 'light',
    type: 'success',
    position: 'bottom-right',
    autoClose: 1000,
  })
}
</script>

<template>
  <main>
    <section>
      <h1 class="section-title">링크</h1>
      <div role="button" class="link-container">
        <div class="link email" @click="copyEmail">
          <img src="../assets/images/at-sign.svg" />
          <span class="link-name">이메일</span><span class="link-id">skurua1244@gmail.com</span>
          <img src="../assets/images/copy.svg" />
        </div>
        <a class="link github" href="https://github.com/skrewbar">
          <img src="../assets/images/github-mark.svg" />
          <span class="link-name">GitHub</span><span class="link-id">skrewbar</span>
          <img src="../assets/images/link.svg" />
        </a>
        <a class="link solvedac" href="https://solved.ac/skuru">
          <img src="https://static.solved.ac/logo.svg" />
          <span class="link-name">solved.ac</span>
          <span class="link-id">skuru</span>
          <img src="../assets/images/link.svg" />
        </a>
      </div>
    </section>
    <section>
      <h1 class="section-title">SNS (안함)</h1>
      <div class="link-container">
        <a class="link instagram" href="https://www.instagram.com/skrew_bar/">
          <img src="../assets/images/instagram.svg" />
          <span class="link-name">Instagram</span><span class="link-id">skrew_bar</span
          ><img src="../assets/images/link.svg"
        /></a>
      </div>
    </section>
  </main>
</template>

<style scoped>
.link-container {
  display: flex;
  flex-direction: column;
}

.link {
  cursor: pointer;

  border: 2px black solid;
  border-radius: 1rem;

  height: 4rem;
  width: 100%;

  margin: 0.5rem 0;

  align-items: center;
  display: flex;

  text-decoration: none;

  color: black;
  font-size: 1.5rem;

  transition: 0.4s;
}

.link-name {
  flex-grow: 1;
}

.link-id {
  text-align: right;
}

.link img {
  height: 2rem;
  margin: 1rem;
}

@media (hover: hover) {
  .link.email:hover {
    background-color: rgb(255, 233, 233);
  }
  .link.github:hover {
    background-color: rgb(207, 207, 207);
  }
  .link.solvedac:hover {
    background-color: rgb(178, 255, 192);
  }
  .link.instagram:hover {
    background-color: #ffabd1;
  }
}
</style>
