<template>
  <div class="tooltip h-full">
    <slot></slot>
    <span class="tooltiptext text-xs md:text-xs lg:text-base">{{ name }}</span>
  </div>
</template>

<script setup>
import { defineProps } from 'vue'
const props = defineProps({
  name: {
    type: String
  }
})
</script>

<style scoped>
.tooltip {
  position: relative;
  display: flex;
  justify-content: center;
}

.tooltip .tooltiptext {
  top: 100%;
  visibility: hidden;
  width: max-content;
  background-color: black;
  color: #fff;
  text-align: center;
  padding: 5px 10px;
  border-radius: 6px;
  position: absolute;
  z-index: 1;
  opacity: 0;
  transform: translateY(-0.8vh);
  transition:
    opacity 0.3s ease-in-out,
    transform 0.3s ease-in-out;
}

.tooltip:hover .tooltiptext {
  visibility: visible;
  opacity: 1;
  transform: translateY(0);
}
</style>
