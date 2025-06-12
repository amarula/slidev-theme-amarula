<script setup>
</script>

<template>
  <div class="slidev-layout flex flex-col h-full w-full p-8 space-y-8 justify-evenly">
    <TopBar v-if="$slots.title">
      <template #pageTitle>
        <slot name="title" />
      </template>
    </TopBar>

    <div class="content">
      <slot name="body" />
    </div>
  </div>

  <BottomBar>
  </BottomBar>
</template>
