<script setup lang="ts"></script>

<template>
  <main>
    <img src="../assets/images/profile.png" />
    <h1>프로필 사진</h1>
    <a href="../assets/images/profile.png" download="profile.png">
      <img class="download" src="../assets/images/download.svg" alt="download" />
      <span>다운로드</span>
    </a>

    <hr />

    <img src="../assets/images/legacyprofile.jpg" />
    <h1>구 프로필 사진</h1>
    <a href="../assets/images/legacyprofile.jpg" download="legacyprofile.jpg">
      <img class="download" src="../assets/images/download.svg" alt="download" />
      <span>다운로드</span>
    </a>
  </main>
</template>

<style scoped>
img {
  max-width: 25vw;
}

a {
  display: flex;
  align-items: center;
  font-size: 2rem;
}
.download {
  height: 2rem;
  margin: 0 0.5rem;
}

hr {
  margin: 2rem 0;
  border-style: dashed;
  color: #9b9b9b;
}
</style>
