<script setup lang="js">
import NavHeader from '../navigation/NavHeader.vue'
import NavBar from '../navigation/NavBar.vue'
</script>

<template>
  <div class="relative">
    <NavHeader />
    <slot></slot>
    <NavBar />
  </div>
</template>
