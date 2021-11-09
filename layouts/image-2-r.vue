<template>
  <default class="table-contents" :logoHeader="logoHeader">
  <div class="slidev-layout two-columns w-full h-full grid grid-cols-2">
    <div class="col-left">
      <slot />
    </div>
    <div class="col-right">
      <div class="flex flex-wrap flex-col">
        <img
          :src="image1"
          alt="Slide image"
          class="rounded-md shadow-lg m-auto object-contain h-full w-full pt-2 pb-2"
        />
        <img
          :src="image2"
          alt="Slide image"
          class="rounded-md shadow-lg m-auto object-contain h-full w-full pt-2 pb-2"
        />
      </div>
    </div>
  </div>
  </default>
</template>

<script setup lang="ts">
import { defineProps, defineComponent } from "vue";
import Default from "slidev-theme-unicorn/layouts/default.vue";

const components = defineComponent({ Default });
const props = defineProps({
  image1: {
    type: String,
  },
  image2: {
    type: String,
  },
});
</script>
slidev-theme-unicorn/layouts/default.vue