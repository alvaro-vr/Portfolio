<template>
  <div id="profile" class="w-full h-[80vh] flex justify-around items-center flex-wrap gap-10">
    <img
      class="md:h-64 lg:h-80 xl:h-3/5 rounded-full border-4 border-neutral-900 border-opacity-30 shadow-black shadow-2xl"
      src="/profile.png"
      :alt="profile.name"
    />
    <div>
      <h1
        class="text-neutral-900 mt-3 text-4xl xl:text-6xl font-medium text-center transition-all duration-1000 hover:scale-150 hover:xl:scale-125 hover:mb-3"
      >
        {{ profile.name }}
      </h1>
      <h2 class="text-neutral-600 text-xl xl:text-3xl font-medium text-center">
        {{ profile.title }}
      </h2>
    </div>
    <div class="flex flex-wrap h-10 lg:h-12 xl:h-16 [&>*]:mx-6">
      <ToolTip :name="'GitHub'">
        <GitHubIcon
          class="text-neutral-800 transition duration-500 hover:rotate-6"
          :github="profile.github"
        />
      </ToolTip>
      <ToolTip :name="'Linkedin'">
        <LinkedinIcon
          class="text-blue-700 transition duration-500 hover:rotate-6"
          :linkedin="profile.linkedin"
        />
      </ToolTip>
    </div>
  </div>
</template>

<script setup>
import LinkedinIcon from '../icons/LinkedinIcon.vue'
import GitHubIcon from '../icons/GitHubIcon.vue'
import ToolTip from '../utils/ToolTip.vue'
import { defineProps } from 'vue'

defineProps({
  profile: {
    type: Object
  }
})
</script>
