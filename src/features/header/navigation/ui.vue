<script setup lang="ts">
import { RouterLink } from 'vue-router'
import { Typography } from '@/shared/typography'
import { Icon } from '@/shared/icon'
interface Props {
  data: {
    label: string
    icon: string
    count: number
    link: string
  }[]
}
const { data } = defineProps<Props>()
</script>

<template>
  <nav class="header-navigation">
    <ul class="header-navigation__list">
      <li v-for="item in data" :key="item.label" class="list__item">
        <RouterLink :to="item.link" class="item">
          <Icon :type="item.icon" />
          <Typography tagName="span" size="xs">{{ item.label }}</Typography>
          <span v-if="item.count > 0" class="item__count">{{ item.count }}</span>
        </RouterLink>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
.header-navigation__list {
  display: flex;
  grid-gap: 24px;
}
.item {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  grid-gap: 8px;
  text-decoration: none;
}

.item__count {
  position: absolute;
  top: -9px;
  right: 6px;
  padding: 0px 4px;
  font-size: 12px;
  background-color: var(--main-primary);
  color: var(--main-on-primary);
  border-radius: 6px;
}
</style>
