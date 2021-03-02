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
  <nav class="text-xl mb-6">
    <router-link class="icon-btn mx-2" to="/" :title="t('button.home')">
      <carbon-campsite />
    </router-link>

    <a class="icon-btn mx-2" rel="noreferrer" href="https://thien.gg/blog" target="_blank" title="GitHub">
      <ion-journal-outline/>
    </a>
    <a class="icon-btn mx-2" rel="noreferrer" href="https://github.com/thnmtrn" target="_blank" title="GitHub">
      <mdi-folder-open/>
    </a>

    <a class="icon-btn mx-2" :title="t('button.toggle_dark')" @click="toggleDark">
      <carbon-moon v-if="isDark" />
      <carbon-sun v-else />
    </a>

    <a class="icon-btn mx-2" :title="t('button.toggle_langs')" @click="toggleLocales">
      <carbon-language />
    </a>

    <router-link class="icon-btn mx-2" to="/about" :title="t('button.about')">
      <carbon-dicom-overlay />
    </router-link>

   <router-link class="icon-btn mx-2" to="/bookmark" :title="bookmark">
      <carbon-bookmark />
    </router-link>

  </nav>
</template>
