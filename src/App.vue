<script setup lang="ts">
import {
  ArrowDownIcon,
  ArrowLeftIcon,
  ArrowRightIcon,
  ArrowUpIcon,
} from "@heroicons/vue/24/outline";
</script>

<template>
  <main
    class="flex h-screen items-center justify-center gap-x-4 dark:bg-slate-900"
  >
    <ArrowUpIcon
      class="h-12 w-12 rounded-full stroke-white transition-[background-color] dark:bg-blue-500 hover:dark:bg-green-500"
    ></ArrowUpIcon>
    <ArrowRightIcon
      class="h-12 w-12 rounded-full stroke-white transition-[background-color] dark:bg-blue-500 hover:dark:bg-green-500"
    ></ArrowRightIcon>
    <ArrowDownIcon
      class="h-12 w-12 rounded-full stroke-white transition-[background-color] dark:bg-blue-500 hover:dark:bg-green-500"
    ></ArrowDownIcon>
    <ArrowLeftIcon
      class="h-12 w-12 rounded-full stroke-white transition-[background-color] dark:bg-blue-500 hover:dark:bg-green-500"
    ></ArrowLeftIcon>
  </main>
</template>

<style>
@import "tailwindcss/base";
@import "tailwindcss/components";
@import "tailwindcss/utilities";
</style>
