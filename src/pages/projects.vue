<script setup lang="ts">
import { ref } from 'vue'
import { useRouter } from 'vue-router'
import { useI18n } from 'vue-i18n'

const name = ref('/projects')

const router = useRouter()


const { t } = useI18n()
</script>

<template>
  <div>
      projects




  </div>
</template>

<route lang="yaml">
meta:
  layout: home
</route>
