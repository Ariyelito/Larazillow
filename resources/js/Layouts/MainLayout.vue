<template>
  <Link href="/">Home</Link>&nbsp;
  <Link href="/hello">Show Page</Link>
  <div>The page with the timer {{ timer }}</div>
  <slot>Loading...</slot>
</template>

<script setup>
import { Link } from '@inertiajs/inertia-vue3'
import { ref } from 'vue'

const timer = ref(0)
setInterval(() => timer.value++, 1000)
</script>