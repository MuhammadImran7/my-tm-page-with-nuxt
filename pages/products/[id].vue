<script setup>
const { id } = useRoute().params
const uri = 'https://fakestoreapi.com/products/' + id
//fetch product
const { data: product } = await useFetch(uri, { key: id })
definePageMeta({
    layout: 'products'
})

if (!product.value) {
    throw createError({ statusCode: 404, statusMessage: 'Product Not Found', fatal:true})
}
</script>

<template>
    <div>
        <ProductDetails :product="product"></ProductDetails>
    </div>
</template>

<style scoped>

</style>