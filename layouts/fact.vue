<script setup lang="ts">
import { isDark } from '@slidev/client/logic/dark.ts'
</script>

<template>
  <div class="slidev-layout fact">
    <img src="../images/logo-small-white.svg" class="logo-topright" v-if="isDark" />
    <img src="../images/logo-small-white.svg" class="logo-topright" v-else />
    <div class="my-auto">
      <slot />
    </div>
  </div>
  <table class="bottompanel">
      <tr>
        <th style="text-align:left; padding-left:8px">
          <a href="https://www.amarulasolutions.com">https://www.amarulasolutions.com</a>
        </th>
        <th>
          <SlideCurrentNo />
        </th>
      </tr>
  </table>
</template>
