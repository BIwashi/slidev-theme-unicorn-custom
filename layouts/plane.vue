<template>
  <div class="plane slidev-layout">
    <slot />
  </div>
</template>

<script setup lang="ts">
import { defineProps, defineComponent } from "vue";
import Snow from '../layouts/snow.vue'

const components = defineComponent({ Snow });
const props = defineProps({
  snow:{
    type: Boolean,
    required: false,
  }
})
</script>
