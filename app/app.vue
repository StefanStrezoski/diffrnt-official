<script setup lang="ts">
useHead({
  titleTemplate: title => (title ? `${title} · DIFFRNT` : 'DIFFRNT — Independent Record Label'),
})

useSeoMeta({
  description: 'DIFFRNT is an independent record label championing artists who sound like no one else.',
  ogSiteName: 'DIFFRNT',
  ogType: 'website',
})
</script>

<template>
  <NuxtPage />
</template>
