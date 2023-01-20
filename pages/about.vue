<template>
  <div>
    <h2>About</h2>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusamus labore temporibus nihil amet veritatis sit
      omnis, animi cum doloremque. Doloremque expedita molestiae sapiente, debitis facilis sed incidunt quis. Numquam,
      sapiente.
    </p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusamus labore temporibus nihil amet veritatis sit
      omnis, animi cum doloremque. Doloremque expedita molestiae sapiente, debitis facilis sed incidunt quis. Numquam,
      sapiente.
    </p>
    <div>{{ data }}</div>
  </div>
</template>

<script setup>
const { data } = await useFetch('/api/ninja?name=mario')
</script>

<style scoped>
h2 {
  margin-bottom: 1rem;
  font-size: 36px;
}

p {
  margin: 20px 0;
}
</style>