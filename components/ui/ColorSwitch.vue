<template>
  <button @click="switchColor" class="bg-transparent b-hidden flex inline-block cursor-pointer mr0"
    aria-label="Color Switcher">
    <Icon v-if="$colorMode.preference === 'dark'" class="h4.5 w4.5 text-white dark:text-black" name="uil:sun" />
    <Icon v-else class="h5 w5 dark:text-black text-white" name="uil:moon" />
  </button>
</template>
<script setup lang="ts">
const c = useColorMode();

function switchColor() {
  c.preference = c.value === "dark" ? "light" : "dark";
}
</script>
