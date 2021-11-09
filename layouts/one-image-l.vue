<template>
  <default class="table-contents" :logoHeader="logoHeader">
    <div class="flex items-center">
      <div class="w-1/2">
        <img
          :src="image"
          alt="Slide image"
          class="rounded-md shadow-lg m-auto object-contain h-full w-full"
        />
      </div>
      <div class="w-1/2 pl-6 self-end justify-center">
        <slot />
      </div>
    </div>
  </default>
</template>

<script setup lang="ts">
import { defineProps, defineComponent } from "vue";
import Default from "slidev-theme-unicorn/layouts/default.vue";

const components = defineComponent({ Default });
const props = defineProps({
  image: {
    type: String,
  },
});
</script>
slidev-theme-unicorn/layouts/default.vue