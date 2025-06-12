<script>
import { useDarkMode } from '@slidev/client'

const { isDark } = useDarkMode()
</script>

<template>
    <div class="top-bar flex flex-row space-x-8 items-end">
        <img :src="isDark ? '../images/logo-small-white.svg' : '../images/logo-small-dark.svg'"
            class="w-16 ml-4" alt="Amarula Logo" />

        <div class="w-full flex-col">
            <div class="title text-3xl -my-2">
                <slot name="pageTitle" />
            </div>
            <div class="bg-accent divider rounded-sm"></div>
        </div>
    </div>
</template>

<style scoped>
.divider {
    width: 98%;
    height: 4px;
}
</style>