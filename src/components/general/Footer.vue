<template>
  <footer
    id="footer"
    class="flex justify-center mt-20 w-full bg-neutral-500 bg-opacity-20 px-10 py-5"
  >
    <p class="text-neutral-900">
      {{ profile.email }} | ©2024 | Made with Vue.js |
      <a :href="profile.linkedin" target="_blank">Linkedin</a> |
      <a :href="profile.github" target="_blank">Github</a>
    </p>
  </footer>
</template>

<script setup>
import { defineProps } from 'vue'

defineProps({
  profile: {
    type: Object
  }
})
</script>

<style>
footer > p > a {
  color: blue !important;
  text-decoration: underline;
}
</style>
