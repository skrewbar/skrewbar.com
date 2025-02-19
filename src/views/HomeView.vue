<script setup lang="ts"></script>

<template>
  <main>
    <!-- TODO
     PS
     마인크래프트 플러그인 개발
     관련해서 적기
     -->
    <img class="avatar" src="https://avatars.githubusercontent.com/u/66629525?v=4" />
    <h1 class="title">안녕하세요, 코딩을 좋아하는 스쿠루입니다!</h1>
    <h1><span class="rainbow">만들고 싶은 걸</span> 만들고 있습니다.</h1>
  </main>
</template>

<style scoped>
.avatar {
  border-radius: 50%;
  width: 12rem;
}

.rainbow {
  font-weight: bold;
  background: linear-gradient(
    to right,
    #ef5350,
    #f48fb1,
    #7e57c2,
    #2196f3,
    #26c6da,
    #43a047,
    #eeff41,
    #f9a825,
    #ff5722
  );
  background-clip: text;
  color: transparent;
}
</style>
