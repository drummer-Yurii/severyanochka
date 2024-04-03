<script setup lang="ts">
interface Props {
  leftIcon?: HTMLElement
  rightIcon?: HTMLElement
  color?: 'primary' | 'secondary' | 'grayscale' | 'error'
  decoration?: 'default' | 'outline' | 'none'
  size?: 'L' | 'M' | 'S'
  disabled?: boolean
}

const props = defineProps<Props>()

const {
  leftIcon = null,
  rightIcon = null,
  color = 'primary',
  decoration = 'default',
  size = 'M',
  disabled = false
} = props
</script>

<template>
  <button></button>
</template>

<style scoped></style>
