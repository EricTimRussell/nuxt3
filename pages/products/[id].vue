<template>
  <div>
    <p>Product details for {{ id }}</p>
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Tempora molestias eaque vel incidunt repudiandae dolor,
      porro corporis amet quod quisquam officia dolorum quis non cupiditate. Consequuntur corporis pariatur ducimus
      doloribus?</p>
  </div>
</template>

<script setup>
const { id } = useRoute().params
definePageMeta({
  layout: 'products'
})
</script>

<style lang="scss" scoped>

</style>