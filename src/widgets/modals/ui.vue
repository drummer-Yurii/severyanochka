<script lang="ts" setup>
import { ModalSignIn } from '@/features/modals/modal-sign-in';
import { type ModalsProps } from './types.ts';
const { items } = defineProps<ModalsProps>();
</script>

<template>
  <div class="modals">
    <ModalSignIn v-if="items.includes('sign-in')" />
  </div>
</template>

<style scoped></style>
