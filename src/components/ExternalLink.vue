<script setup lang="ts">
defineProps<{
  linkAdress: string
  linkImg?: string
  linkName: string
  linkId: string
  backgroundColor: string
}>()
</script>

<template>
  <a class="link" :href="linkAdress">
    <img :src="linkImg" />
    <span class="link-name">{{ linkName }}</span
    ><span class="link-id">{{ linkId }}</span>
    <img src="../assets/images/link.svg" />
  </a>
</template>

<style scoped>
.link {
  cursor: pointer;

  border: 2px black solid;
  border-radius: 1rem;

  height: 4rem;
  width: 100%;

  margin: 0.5rem 0;
  padding: 0;

  align-items: center;
  display: flex;

  text-decoration: none;

  color: black;
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
