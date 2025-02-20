<script setup lang="ts">
import CopyLink from '@/components/CopyLink.vue';
import ExternalLink from '@/components/ExternalLink.vue'

import gitHubIcon from '@/assets/images/github-mark.svg'
import instagramIcon from '@/assets/images/instagram.svg'
import atSignIcon from '@/assets/images/at-sign.svg'
</script>

<template>
  <main>
    <section>
      <h1 class="section-title">링크</h1>
      <div role="button" class="link-container">
        <CopyLink
          :link-img="atSignIcon"
          link-name="이메일"
          link-id="skurua1244@gmail.com"
          background-color="rgb(255, 233, 233)"
        />
        <ExternalLink
          link-adress="https://github.com/skrewbar"
          :link-img="gitHubIcon"
          link-name="GitHub"
          link-id="skrewbar"
          background-color="rgb(207, 207, 207)"
        />
        <ExternalLink
          link-adress="https://solved.ac/skuru"
          link-img="https://static.solved.ac/logo.svg"
          link-name="solved.ac"
          link-id="skuru"
          background-color="rgb(178, 255, 192)"
        />
      </div>
    </section>
    <section>
      <h1 class="section-title">SNS (안함)</h1>
      <div class="link-container">
        <ExternalLink
          link-adress="https://www.instagram.com/skrew_bar/"
          :link-img="instagramIcon"
          link-name="Instagram"
          link-id="skrew_bar"
          background-color="rgb(255, 171, 209)"
        />
      </div>
    </section>
  </main>
</template>

<style scoped>
.link-container {
  display: flex;
  flex-direction: column;
}
</style>
