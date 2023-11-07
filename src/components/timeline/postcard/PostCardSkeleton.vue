<script setup lang="js">
import { Icon } from '@iconify/vue'
</script>

<template>
  <main class="flex flex-col gap-3">
    <section class="flex items-center px-3 gap-2 animate-pulse">
      <div class="h-6 w-6 bg-gray-400 rounded-full"></div>
      <div class="bg-gray-400 w-20 h-2 rounded-full"></div>
    </section>
    <div class="w-full h-[375px] bg-gray-400 animate-pulse" />
    <div class="flex gap-2 px-4 text-xl">
      <Icon icon="mdi:heart-outline" />
      <Icon icon="mynaui:chat" />
      <Icon icon="iconamoon:send-light" />
    </div>
    <section class="px-4 flex flex-col gap-2 animate-pulse">
      <div class="bg-gray-400 w-full h-2"></div>
      <div class="bg-gray-400 w-full h-2"></div>
      <div class="bg-gray-400 w-full h-2"></div>
    </section>
  </main>
</template>
