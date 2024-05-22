<template>
  <div id="proyects" class="flex flex-col w-full gap-10">
    <h2 class="text-4xl font-medium">{{ proyects.title }}</h2>
    <div id="list-proyects" class="grid grid-cols-2 gap-10 max-md:grid-cols-1">
      <ProyectCard v-for="proyect in proyects.list" :proyect="proyect" />
    </div>
  </div>
</template>

<script setup>
import ProyectCard from '@/components/utils/ProyectCard.vue'
import { defineProps } from 'vue'

defineProps({
  proyects: {
    type: Object
  }
})
</script>
