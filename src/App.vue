<template>
  <div id="container" class="flex flex-col items-center max-w-7xl px-10">
    <Profile :profile="data.profile" />
    <Separator />
    <AboutMe :aboutme="data.aboutme" />
    <Separator />
    <Proyects :proyects="data.proyects" />
    <Separator />
    <Technologies />
    <Footer :profile="data.profile" />
  </div>
</template>

<script setup>
import Profile from '@/components/general/Profile.vue'
import Separator from '@/components/general/Separator.vue'
import AboutMe from '@/components/general/AboutMe.vue'
import Footer from '@/components/general/Footer.vue'
import Proyects from '@/components/general/Proyects.vue'
import Technologies from '@/components/general/Technologies.vue'

import data from '@/data.json'
</script>
