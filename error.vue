<template>
  <div class="text-center card">
    <p class="my-7 text-7xl font-bold">{{ error.statusCode }}</p>
    <p class="text-6xl">Oooops.</p>
    <p class="mt-7">{{ error.message }}</p>
    <button @click="handleClearError" class="btn my-7">Go Home...</button>
  </div>
</template>

<script setup>
defineProps(['error'])

const handleClearError = () => clearError({ redirect: '/' })
</script>

<style scoped>

</style>