<script setup>
    const { product } = defineProps(['product'])
</script>

<template>
    <div class="card p-3 rounded-md bg-white shadow-md h-full text-center flex flex-col items-center">
        <img :src="product.image" alt="product thumb" class="thumb h-24 w-24">
        <p class="font-bold text-gray-500 n-4">{{ product.title }}</p>
        <NuxtLink :to="`/products/${product.id}`">
            <p class="btn bg-[#12b488] text-white px-3 py-2 rounded-md text-sm my-4">View Details</p>
        </NuxtLink>
    </div>
</template>

<style scoped>

</style>