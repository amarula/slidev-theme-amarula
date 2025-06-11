<script setup lang="ts">
import { isDark } from '@slidev/client/logic/dark.ts'
</script>

<template>
  <div class="slidev-layout intro">
    <img src="../images/logo-small-white.svg" class="logo-topright" v-if="isDark" />
    <img src="../images/logo-small-dark.svg" class="logo-topright" v-else />
    <div class="my-auto">
      <slot />
    </div>
  </div>
</template>
