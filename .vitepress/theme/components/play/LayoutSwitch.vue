<script setup lang="ts">
import { defineProps } from 'vue'
import { layout } from '../../composables/playgroundLayout'

defineProps({
  open: Boolean,
})
</script>

<template>
  <div class="relative hidden md:block" @click.stop="$emit('toggle')">
    <NavBarIcon title="Switch layout" alt="Switch layout">
      <carbon:open-panel-right />
    </NavBarIcon>
    <div v-if="open" class="dropdown-model">
      <NavBarIcon v-if="layout !== 'left'" @click="layout = 'left'">
        <carbon:open-panel-left />
      </NavBarIcon>
      <NavBarIcon v-if="layout !== 'bottom'" @click="layout = 'bottom'">
        <carbon:open-panel-bottom />
      </NavBarIcon>
      <NavBarIcon v-if="layout !== 'right'" @click="layout = 'right'">
        <carbon:open-panel-right />
      </NavBarIcon>
    </div>
  </div>
</template>

<style scoped lang="postcss">
.dropdown-model {
  @apply
  grid gap-2 p-1.5
  absolute top-11 -left-2
  bg-white dark:bg-dark-700
  rounded-lg border border-blue-gray-200 dark:border-dark-300;
}
</style>
