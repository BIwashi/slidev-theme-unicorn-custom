<template>
  <default class="image-center">
    <slot />
    <div class="flex flex-wrap flex-row">
      <div class="w-1/2 pl-2 pr-2">
        <img
          :src="image1"
          alt="Slide image"
          class="rounded-md shadow-lg m-auto object-contain h-full w-full"
        />
      </div>
      <div class="w-1/2 pl-2 pr-2">
        <img
          :src="image2"
          alt="Slide image"
          class="rounded-md shadow-lg m-auto object-contain h-full w-full"
        />
      </div>
    </div>
  </default>
</template>

<script setup lang="ts">
import { defineProps, defineComponent } from "vue";
import Default from "slidev-theme-unicorn/layouts/default.vue";

const components = defineComponent({ Default});
const props = defineProps({
  image1: {
    type: String,
  },
  image2: {
    type: String,
  },
});
</script>
