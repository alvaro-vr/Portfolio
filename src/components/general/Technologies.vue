<template>
  <div class="flex flex-col w-full gap-10">
    <h1 class="text-3xl">Tecnologías</h1>
    <div class="flex flex-wrap gap-10">
      <div
        v-for="tech in technologies"
        :key="tech.category"
        class="flex flex-col font-semibold gap-5 bg-white rounded-xl px-3 py-2 shadow-xl max-sm:w-full"
      >
        <h2 class="text-2xl">{{ tech.category }}</h2>
        <div class="flex flex-wrap h-auto gap-7">
          <component
            v-for="iconName in tech.icons"
            :key="iconName"
            :is="iconsMap[iconName]"
            class="h-12 w-12"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineAsyncComponent } from 'vue'
// Define an asynchronous import function for icons
const iconsMap = {
  JavaIcon: defineAsyncComponent(() => import('@/components/icons/back/JavaIcon.vue')),
  SpringIcon: defineAsyncComponent(() => import('@/components/icons/back/SpringIcon.vue')),
  NodeIcon: defineAsyncComponent(() => import('@/components/icons/back/NodeIcon.vue')),

  VueIcon: defineAsyncComponent(() => import('@/components/icons/front/VueIcon.vue')),
  NuxtIcon: defineAsyncComponent(() => import('@/components/icons/front/NuxtIcon.vue')),
  TailwindIcon: defineAsyncComponent(() => import('@/components/icons/front/TailwindIcon.vue')),
  JavascriptIcon: defineAsyncComponent(() => import('@/components/icons/front/JavascriptIcon.vue')),

  MySqlIcon: defineAsyncComponent(() => import('@/components/icons/db/MySqlIcon.vue')),

  DockerIcon: defineAsyncComponent(() => import('@/components/icons/other/DockerIcon.vue')),
  GitIcon: defineAsyncComponent(() => import('@/components/icons/other/GitIcon.vue')),
  NpmIcon: defineAsyncComponent(() => import('@/components/icons/other/NpmIcon.vue')),
  VSCodeIcon: defineAsyncComponent(() => import('@/components/icons/other/VSCodeIcon.vue')),
  PostmanIcon: defineAsyncComponent(() => import('@/components/icons/other/PostmanIcon.vue'))
}

const technologies = [
  {
    category: 'Back-end',
    icons: ['JavaIcon', 'SpringIcon', 'NodeIcon']
  },
  {
    category: 'Front-End',
    icons: ['JavascriptIcon', 'VueIcon', 'NuxtIcon', 'TailwindIcon']
  },
  {
    category: 'DB',
    icons: ['MySqlIcon']
  },
  {
    category: 'Other',
    icons: ['DockerIcon', 'GitIcon', 'NpmIcon', 'VSCodeIcon', 'PostmanIcon']
  }
]
</script>
