<script setup>
import { useDarkMode } from '@slidev/client'

const { isDark } = useDarkMode()

// Constants for length thresholds
const TITLE_LONG = 80
const TITLE_MEDIUM = 50

function getTitleSizeClass(title = '') {
  const len = title.length
  if (len > TITLE_LONG) return 'text-3xl'
  if (len > TITLE_MEDIUM) return 'text-4xl'
  return 'text-5xl'
}

function getDividerWidthClass(title = '') {
  return title.length > TITLE_LONG ? 'w-4' : 'w-2'
}

const logoDark = new URL('../assets/logo-small-dark.svg', import.meta.url).href
const logoWhite = new URL('../assets/logo-small-white.svg', import.meta.url).href
</script>

<template>
  <div class="slidev-layout w-full h-full p-8 flex flex-col justify-between">

    <!-- Event Header -->
    <div class="text-3xl font-semibold">
      {{ $slidev.configs.event || '' }}
    </div>

    <!-- Main Content -->
    <div class="flex flex-row justify-center items-center space-x-16">

      <!-- Logo -->
      <img :src="isDark ? logoWhite : logoDark" class="w-64"
        alt="Amarula Logo" />

      <!-- Divider -->
      <div :class="[getDividerWidthClass($slidev.configs.title), 'bg-accent rounded-sm h-full mx-8']"></div>

      <!-- Text Content -->
      <div class="flex flex-col justify-center space-y-4 text-left">

        <!-- Title -->
        <div :class="[getTitleSizeClass($slidev.configs.title), 'font-bold leading-tight']">
          {{ $slidev.configs.title || '' }}
        </div>

        <!-- Author -->
        <div class="text-3xl font-medium">
          {{ $slidev.configs.author || '' }}
        </div>

        <!-- Website -->
        <div class="text-2xl text-blue-500 italic">
          <a href="https://www.amarulasolutions.com/" target="_blank" rel="noopener">
            www.amarulasolutions.com
          </a>
        </div>
      </div>

    </div>

    <!-- Footer -->
    <div class="text-center text-sm font-light mt-4">
      Slides under Creative Commons license BY-SA 3.0.
    </div>
  </div>
</template>
