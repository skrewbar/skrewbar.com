<script setup lang="ts">
import { toast } from 'vue3-toastify'
import 'vue3-toastify/dist/index.css'

const props = withDefaults(
  defineProps<{
    color?: string
    linkImg?: string
    linkName: string
    linkId: string
    backgroundColor?: string
  }>(),
  {
    color: 'black',
    backgroundColor: 'gray',
  },
)

function copyEmail() {
  navigator.clipboard.writeText(props.linkId)
  toast('이메일이 클립보드에 복사되었습니다!', {
    theme: 'light',
    type: 'success',
    position: 'bottom-right',
    autoClose: 1000,
  })
}
</script>

<template>
  <div class="link" @click="copyEmail">
    <img :src="linkImg" />
    <span class="link-name">{{ linkName }}</span
    ><span class="link-id">{{ linkId }}</span>
    <img src="../assets/images/copy.svg" />
  </div>
</template>

<style scoped>
.link {
  cursor: pointer;

  border: 2px v-bind(color) solid;
  border-radius: 1rem;

  height: 4rem;
  width: 100%;

  margin: 0.5rem 0;
  padding: 0;

  align-items: center;
  display: flex;

  text-decoration: none;

  color: v-bind(color);
  font-size: 1.5rem;

  transition: 0.4s;
}
@media (hover: hover) {
  .link:hover {
    background-color: v-bind('backgroundColor');
  }
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
</style>
