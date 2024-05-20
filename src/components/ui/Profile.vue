<template>
  <div class="h-auto w-full p-[5vh]">
    <img
      class="w-full h-full rounded-full border-[1vh] border-yellow-200 border-opacity-30"
      src="../../assets/images/profile.png"
      :alt="data.profile.name"
    />
    <h1
      class="text-neutral-700 mt-3 text-4xl font-semibold text-center underline underline-offset-8"
    >
      {{ data.profile.name }}
    </h1>
  </div>
  <div class="flex justify-center h-16 [&>*]:mx-6">
    <ToolTip :name="'GitHub'">
      <GitHubIcon class="text-neutral-800" :data="data" />
    </ToolTip>
    <ToolTip :name="'Linkedin'">
      <LinkedinIcon class="text-blue-700" :data="data" />
    </ToolTip>
  </div>
</template>

<script setup>
import LinkedinIcon from '../icons/LinkedinIcon.vue'
import GitHubIcon from '../icons/GitHubIcon.vue'
import ToolTip from '../utils/ToolTip.vue'
import data from '@/data.json'
</script>
