<script setup lang="ts">
import Container from '@/shared/container/index.vue'
import Logo from '@/shared/logo/index.vue'
</script>
<template>
  <header class="header">
    <Container class="header__container">
      <Logo orientation="horizontal" bgColor="white" colorFull withText />
    </Container>
  </header>
</template>

<style scoped>
.header__container {
  display: flex;
  align-items: center;
  height: 72px;
}

.header {
  position: sticky;
  top: 0;
  left: 0;
  background: var(--surface);
  box-shadow: var(--shadow-default-s);
}
</style>
