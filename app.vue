<template>
  <div>
    <div>
      <p>{{ hello.data?.value?.greeting }}</p>
    </div>
  </div>
</template>

<script setup lang="ts">
const { $trpc } = useNuxtApp()
const hello = await $trpc.hello.useQuery({ text: 'vercel' })
</script>
