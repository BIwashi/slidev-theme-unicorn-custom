<!--
  Usage:

```md
---
layout: two-cols
---

# Left

This shows on the left

::right::

# Right

This shows on the right
```

-->

<template>
  <default class="image-center">
    <div class="slidev-layout two-columns w-full h-full grid grid-cols-2">
      <div class="col-left" :class="props.class">
        <slot />
        <div v-if="image1" class="pl-2 pr-4">
          <img
            :src="image1"
            alt="Slide image"
            class="rounded-md shadow-lg m-auto object-contain h-full w-full"
          />
        </div>
      </div>
      <div class="col-right" :class="props.class">
        <slot name="right" />
        <div v-if="image2" class="pl-2 pr-4">
          <img
            :src="image2"
            alt="Slide image"
            class="rounded-md shadow-lg m-auto object-contain h-full w-full"
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
  class: {
    type: String,
  },
  image1: {
    type: String,
    required: false,
  },
  image2: {
    type: String,
    required: false,
  },
});
</script>