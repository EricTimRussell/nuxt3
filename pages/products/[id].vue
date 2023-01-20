<template>
  <div>

    <!-- Dynamic meta tag -->

    <Head>
      <Title>Nuxt Dojo | {{ product.title }}</Title>
      <Meta name="description" :content="product.description" />
    </Head>


    <ProductDetails :product="product" />
  </div>
</template>

<script setup>
const { id } = useRoute().params
const uri = 'https://fakestoreapi.com/products/' + id

// fetch a specific product by its id
const { data: product } = await useFetch(uri, { key: id })

// Throw error.vue message for product id that does not exist
if (!product.value) {
  throw createError({ statusCode: 404, statusMessage: 'Product not found', fatal: true })
}

// Overides the default layout 
definePageMeta({
  layout: 'products'
})
</script>

<style lang="scss" scoped>

</style>