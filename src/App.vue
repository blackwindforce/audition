<script setup lang="ts">
import MyDirection from "@/components/MyDirection.vue";

// http://www.redbana.com/sub/gamescore.asp

// type Direction = Readonly<{
//   direction: "N" | "NE" | "E" | "SE" | "S" | "SW" | "W" | "NW";
//   opposite: boolean;
//   status: boolean;
// }>;

// defineProps<{
//   control: "4-key" | "8-key";
//   ok: boolean;
// }>();

// provide success and success-color?

const states = [
  { direction: "N", opposite: false },
  { direction: "N", opposite: true },
  { direction: "NE", opposite: false },
  { direction: "NE", opposite: true },
  { direction: "E", opposite: false },
  { direction: "E", opposite: true },
  { direction: "SE", opposite: false },
  { direction: "SE", opposite: true },
  { direction: "S", opposite: false },
  { direction: "S", opposite: true },
  { direction: "SW", opposite: false },
  { direction: "SW", opposite: true },
  { direction: "W", opposite: false },
  { direction: "W", opposite: true },
  { direction: "NW", opposite: false },
  { direction: "NW", opposite: true },
] as const;
</script>

<template>
  <main class="grid h-screen place-items-center dark:bg-black">
    <div class="flex items-center gap-x-2">
      <MyDirection
        v-for="(state, index) of states"
        :key="index"
        :direction="state.direction"
        :opposite="state.opposite"
      >
      </MyDirection>
    </div>
  </main>
</template>

<style>
@import "tailwindcss/base";
@import "tailwindcss/components";
@import "tailwindcss/utilities";
</style>
