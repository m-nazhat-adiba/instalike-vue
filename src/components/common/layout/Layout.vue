<script setup lang="js">
import NavBar from '../navigation/NavBar.vue'
</script>

<template>
  <div class="w-[375px] mx-auto">
    <NavBar />
    <slot></slot>
  </div>
</template>
