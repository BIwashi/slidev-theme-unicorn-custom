<template>
  <default class="new-section" :logoHeader="logoHeader">
    <div class="flex items-center">
      <figure class="w-1/2">
        <img :src="sectionImage" alt="new section" class="ml-auto rounded-md shadow-lg h-full w-full" />
      </figure>
      <div class="w-1/2 text-right pr-12">
        <slot />
      </div>
    </div>
  </default>
</template>

<script setup lang="ts">
import { defineProps, defineComponent } from 'vue'
import Default from './default.vue'

const components = defineComponent({ Default })
const props = defineProps({
  sectionImage: {
    type: String,
    default: '../public/section-illustration.svg'
  },
})
</script>

<style>
.slidev-layout.new-section {
  @apply bg-gradient-to-r from-fuchsia-700 to-purple-800 text-white;
}
.slidev-layout.new-section *,
.slidev-layout.new-section h1,
.slidev-layout.new-section h2,
.slidev-layout.new-section h3,
.slidev-layout.new-section h4,
.slidev-layout.new-section h5,
.slidev-layout.new-section h6,
.slidev-layout.new-section p,
.slidev-layout.new-section strong,
.slidev-layout.new-section a { @apply text-white; }
</style>
