<template>
  <div class="bg-white border border-gray-200 rounded-lg shadow-2xl shadow-black">
    <img class="h-60 w-auto rounded-t-lg" :src="proyect.image" :alt="proyect.title" />
    <div class="flex justify-between items-end w-full h-auto px-5 py-3 gap-x-11">
      <div class="flex flex-col">
        <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900">
          {{ proyect.title }}
        </h5>
        <p class="mb-3 font-normal text-gray-700">
          {{ proyect.description }}
        </p>
      </div>
      <ToolTip class="h-12" :name="'Ver el proyecto'">
        <GitHubIcon :github="proyect.link" />
      </ToolTip>
    </div>
  </div>
</template>

<script setup>
import ToolTip from '@/components/utils/ToolTip.vue'
import GitHubIcon from '@/components/icons/GitHubIcon.vue'

import { defineProps } from 'vue'

defineProps({
  proyect: {
    type: Object,
    required: true
  }
})
</script>
