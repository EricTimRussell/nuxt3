<template>
  <div>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="p in products">
        <ProductCard :product="p" />
      </div>
    </div>
  </div>
</template>

<script setup>
import ProductCard from "~~/components/ProductCard.vue";

// Overides the defaul layout 
definePageMeta({
  layout: 'products'
})

// Overides Nuxt config meta tags 
useHead({
  title: 'Nuxt 3 | Merch',
  meta: [
    { name: 'description', content: 'Nuxt 3 Merch' }
  ]
})

// fetch the products from the api
const { data: products } = await useFetch('https://fakestoreapi.com/products')
</script>

<style scoped>

</style>