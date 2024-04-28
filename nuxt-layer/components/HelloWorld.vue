<script setup lang="ts">
import { joinURL } from 'ufo'
const { myLayer } = useAppConfig()
</script>

<template>
  <div>
    <h1 class="text-3xl font-bold underline">Hello World!</h1>
    <pre>{{ joinURL('a', '/b') }}</pre>
  </div>
</template>
