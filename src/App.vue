<template>
  <header class="sticky top-0 z-20 flex items-center justify-between border-b bg-white p-4">
    <a href="#">
      <img src="./assets/img/logo.png" alt="Logo" class="h-9" />
    </a>
    <a href="#" class="text-sm">
      <div v-if="true" class="flex items-center gap-1">
        Day complete!
        <CheckCircleIcon class="h-7 w-7 text-green-500" />
      </div>
      <div v-else class="flex items-center gap-1">
        Progress: <span class="font-mono">50%</span>
        <div class="h-3 w-3 rounded-full bg-red-500"></div>
      </div>
    </a>
  </header>
  
</template>

<script setup>
import { CheckCircleIcon } from '@heroicons/vue/24/solid'
</script>
