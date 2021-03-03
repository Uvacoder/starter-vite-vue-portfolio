<script setup lang="ts">
import { ref } from 'vue'
import { useRouter } from 'vue-router'
import { useI18n } from 'vue-i18n'

const name = ref('')

const router = useRouter()
const go = () => {
  if (name.value)
    router.push(`/hi/${encodeURIComponent(name.value)}`)
}

const { t } = useI18n()
</script>

<template>
  <div>
    <p class="text-4xl">
      <carbon-campsite class="inline-block" />
    </p>
    <p>
      <a rel="noreferrer" href="https://thientran.me" target="_blank">
        thien
      </a>
    </p>
    <p>
      <em class="text-sm opacity-75">{{ t('intro.desc') }}</em>
    </p>

    <div class="py-4" />
    <p>hi im thien</p>
    <p>this is my homepage</p>
    <p>i like things pretty minimalist. take a peek around. let me know what you think. Im always up for a chat.</p>

  </div>
</template>

<route lang="yaml">
meta:
  layout: home
</route>
