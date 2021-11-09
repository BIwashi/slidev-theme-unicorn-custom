<template>
    <div class="bg-main slidev-layout">
      <snow v-if="snow"></snow>
      <layout-header :logoHeader="logoHeader" />
      <div class="my-auto">
        <slot />
      </div>
      <layout-footer :website="website" :handle="handle" />
    </div>
</template>

<script setup lang="ts">
import { defineProps, defineComponent } from "vue";
import LayoutHeader from "../components/LayoutHeader.vue";
import LayoutFooter from "../components/LayoutFooter.vue";
import Snow from "../layouts/snow.vue";

const components = defineComponent({
  LayoutHeader,
  LayoutFooter,
  Snow,
});
const props = defineProps({
  logoHeader: {
    type: String,
  },
  website: {
    type: String,
  },
  handle: {
    type: String,
  },
  snow: {
    type: Boolean,
    required: false,
  },
});
</script>