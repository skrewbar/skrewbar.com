<script setup lang="ts"></script>

<template>
  <main>
    <img class="avatar" src="https://avatars.githubusercontent.com/u/66629525?v=4" />
    <h1 class="title">안녕하세요, 코딩을 좋아하는 스쿠루입니다!</h1>
    <h1 class="title"><span class="rainbow">만들고 싶은 걸</span> 만들고 있습니다.</h1>

    <section id="ps">
      <h1 class="section-title">Problem Solving</h1>
      <p>프로그래밍으로 해결할 수 있는 다양한 문제들을 해결합니다.</p>
      <img
        src="../assets/images/solvedprofile-screenshot.png"
        alt="solved profile"
        class="screenshot"
      />
      <img
        src="../assets/images/bronze5-allsolve.png"
        alt="bronze 5 all solve"
        class="screenshot"
      />
      <figure>
        <figcaption>2025년 2월 19일 기준</figcaption>
        <p>BOJ에 등록된 문제 중 911문제를 해결했고, 존재하는 모든 Bronze V 문제를 해결했습니다.</p>
      </figure>
    </section>

    <h1 class="section-title">마인크래프트/희망 서버</h1>
    <p>희망 서버라는 자그만 마인크래프트 서버에서 여러 플러그인 개발을 담당했습니다.</p>
    <section id="mailplugin">
      <h1 class="section-title">메일 플러그인</h1>
      <figure>
        <img class="screenshot" src="../assets/images/sendmail-screenshot.png" width="50%" />
        <img class="screenshot" src="../assets/images/receivemail-screenshot.png" width="50%" />
        <figcaption>메일 플러그인</figcaption>
      </figure>
      <p>제가 처음으로 완성한 프로젝트입니다.</p>
      <p>그만큼 어려움도 많았지만 많이 배우게 된 계기였습니다.</p>
    </section>
    <section id="efx">
      <h1 class="section-title">각종 무기와 이펙트</h1>
      <p>잡다한 무기들의 능력과 이펙트를 개발했습니다.</p>
      <p>아래 영상의 원형 이펙트를 만드는 것이 가장 힘들었습니다.</p>
      <p>원 하나 그리기 위해 제가 기하를 배우게 될 줄은 몰랐습니다.</p>
      <iframe
        class="fragment fade-in"
        src="https://www.youtube.com/embed/CnkoK96JHF8?si=IvlcfHFjY95-5da8"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        allowfullscreen
      ></iframe>
    </section>
  </main>
</template>

<style scoped>
.avatar {
  border-radius: 50%;
  width: 20%;
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

p {
  font-size: 1.75rem;
}

figcaption {
  font-size: 1.5rem;
}

iframe {
  width: 70vw;
  height: 40vw;

  max-width: 100%;
  max-height: 100%;
}

img.screenshot {
  /* width: 25vw; */
  min-width: 300px;
  max-width: 100%;
}
</style>
