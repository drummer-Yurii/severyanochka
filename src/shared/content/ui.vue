<script setup lang="ts"></script>

<template>
  <main class="main">
    <slot></slot>
  </main>
</template>

<style scoped>
.main {
    min-height: calc(100vh - 126px - 72px);
}
</style>
