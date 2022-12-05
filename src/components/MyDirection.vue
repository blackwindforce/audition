<script setup lang="ts">
import {
  ArrowDownIcon,
  ArrowDownLeftIcon,
  ArrowDownRightIcon,
  ArrowLeftIcon,
  ArrowRightIcon,
  ArrowUpIcon,
  ArrowUpLeftIcon,
  ArrowUpRightIcon,
} from "@heroicons/vue/24/outline";

defineProps<{
  direction: "N" | "NE" | "E" | "SE" | "S" | "SW" | "W" | "NW";
  opposite: boolean;
}>();

const ArrowIcon = {
  N: ArrowUpIcon,
  NE: ArrowUpRightIcon,
  E: ArrowRightIcon,
  SE: ArrowDownRightIcon,
  S: ArrowDownIcon,
  SW: ArrowDownLeftIcon,
  W: ArrowLeftIcon,
  NW: ArrowUpLeftIcon,
};
</script>

<template>
  <div
    :class="[
      'grid',
      'h-9',
      'w-9',
      'place-items-center',
      'rounded-full',
      'transition-[background-color]',
      opposite ? 'rotate-180 dark:bg-red-500' : 'dark:bg-blue-500',
    ]"
  >
    <component
      :is="ArrowIcon[direction]"
      class="h-6 w-6 stroke-white stroke-[4]"
    ></component>
  </div>
</template>
