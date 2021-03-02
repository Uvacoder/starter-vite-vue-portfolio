<script setup lang="ts">
import { useI18n } from 'vue-i18n'
import { isDark, toggleDark } from '~/logics'

const { t, availableLocales, locale } = useI18n()

const toggleLocales = () => {
  // change to some real logic
  const locales = availableLocales
  locale.value = locales[(locales.indexOf(locale.value) + 1) % locales.length]
}
</script>

<template>
  <nav class="text-xl mt-6">

    <a class="icon-btn mx-2" rel="noreferrer" href="https://github.com/thnmtrn" target="_blank" title="GitHub">
      <carbon-logo-github />
    </a>
    <a class="icon-btn mx-2" rel="noreferrer" href="https://github.com/thnmtrn" target="_blank" title="GitHub">
      <carbon-logo-linkedin />
    </a>
    <a class="icon-btn mx-2" rel="noreferrer" href="https://github.com/thnmtrn" target="_blank" title="GitHub">
      <carbon-logo-instagram />
    </a>
    <a class="icon-btn mx-2" rel="noreferrer" href="https://github.com/thnmtrn" target="_blank" title="GitHub">
      <carbon-logo-twitter />
    </a>
    <a class="icon-btn mx-2" rel="noreferrer" href="https://github.com/thnmtrn" target="_blank" title="GitHub">
      <simple-icons-freecodecamp />
    </a>
    <a class="icon-btn mx-2" rel="noreferrer" href="https://github.com/thnmtrn" target="_blank" title="GitHub">
      <bi-discord />
    </a>
    <a class="icon-btn mx-2" rel="noreferrer" href="https://github.com/thnmtrn" target="_blank" title="GitHub">
      <grommet-icons:slack />
    </a>

    <a class="icon-btn mx-2" rel="noreferrer" href="https://github.com/thnmtrn" target="_blank" title="GitHub">
      <mdi-email-outline />
    </a>
    <a class="icon-btn mx-2" rel="noreferrer" href="https://github.com/thnmtrn" target="_blank" title="GitHub">
      <mdi-dev-to />
    </a>
  </nav>
</template>
