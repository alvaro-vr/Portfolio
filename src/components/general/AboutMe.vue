<template>
  <div class="flex items-center gap-10">
    <div>
      <h2 class="text-4xl font-medium">{{ aboutme.title }}</h2>
      <br />
      <p class="text-lg">{{ aboutme.description }}</p>
    </div>
    <GrommetIcon class="hidden lg:block" />
  </div>
</template>

<script setup>
import { defineProps } from 'vue'
import GrommetIcon from '../icons/GrommetIcon.vue'

defineProps({
  aboutme: {
    type: Object
  }
})
</script>
