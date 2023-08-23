<template>
  <a
    :href="url"
    class="w-full p-4 rounded-md border border-slate-500 bg-neutral-700 text-white"
    target="_blank"
    ref="noopenner noreferrer"
  >
    <img class="" :src="image" alt="stub-image" />
    <h2 class="text-xl font-bold">{{ title }}</h2>
  </a>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  props: {
    title: {
      type: String,
      required: true,
    },
    image: {
      type: String,
      required: true,
    },
    url: {
      type: String,
      required: true,
    },
  },
  setup() {
    return {};
  },
});
</script>

<style scoped></style>
