<script setup>
definePageMeta({
    layout: 'products'
})
//fetch the products 
const { data: products } = await useFetch('https://fakestoreapi.com/products')
</script>

<template>
    <div class="grid grid-cols-4 gap-5">
        <div v-for="p in products">
            <ProductCard :product="p" />
            <!-- <ProductDetails :product="p" /> -->
        </div>
    </div>
</template>

<style scoped>

</style>