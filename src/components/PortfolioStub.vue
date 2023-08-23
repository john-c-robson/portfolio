<template>
  <a
    :href="url"
    class="w-full h-72 p-4 rounded-md border border-slate-500 bg-neutral-700 text-white"
    target="_blank"
    ref="noopenner noreferrer"
  >
    <div
      class="w-full h-[82%] bg-cover"
      :style="`background-image: url(${image})`"
    >
      <!-- <img class="w-full" :src="image" alt="stub-image" /> -->
    </div>
    <h2 class="font-bold pt-2">{{ title }}</h2>
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
