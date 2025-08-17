<script setup lang="ts">
import CopyLink from '@/components/CopyLink.vue'
import ExternalLink from '@/components/ExternalLink.vue'

import gitHubIcon from '@/assets/images/github-mark.svg'
import gitHubWhiteIcon from '@/assets/images/github-mark-white.svg'
import instagramIcon from '@/assets/images/instagram.svg'
import atSignIcon from '@/assets/images/at-sign.svg'

const isLightTheme: boolean =
  window.matchMedia && window.matchMedia('(prefers-color-scheme: light)').matches
</script>

<template>
  <main>
    <section>
      <h1 class="section-title">링크</h1>
      <div role="button" class="link-container">
        <CopyLink
          color="#FF7C7C"
          :link-img="atSignIcon"
          link-name="이메일"
          link-id="skurua1244@gmail.com"
          background-color="rgb(255, 233, 233)"
        />
        <ExternalLink
          v-if="isLightTheme"
          color="black"
          link-adress="https://github.com/skrewbar"
          :link-img="gitHubIcon"
          link-name="GitHub"
          link-id="skrewbar"
          background-color="rgb(207, 207, 207)"
        />
        <ExternalLink
          v-else
          color="white"
          link-adress="https://github.com/skrewbar"
          :link-img="gitHubWhiteIcon"
          link-name="GitHub"
          link-id="skrewbar"
          background-color="rgb(207, 207, 207)"
        />
        <ExternalLink
          color="#17CE3A"
          link-adress="https://solved.ac/skuru"
          link-img="https://static.solved.ac/logo.svg"
          link-name="solved.ac"
          link-id="skuru"
          background-color="rgb(178, 255, 192)"
        />
      </div>
    </section>
    <section>
      <h1 class="section-title">SNS</h1>
      <div class="link-container">
        <ExternalLink
          color="#FF68AE"
          link-adress="https://www.instagram.com/skrew_bar/"
          :link-img="instagramIcon"
          link-name="Instagram"
          link-id="skrew_bar"
          background-color="#FFCCE3"
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
