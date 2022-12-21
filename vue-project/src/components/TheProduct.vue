<script setup>
    import ProductItem from './ProductItem.vue';
    import TheImage from './TheImage.vue';

    fetch('https://fakestoreapi.com/products/1')
            .then(res=>res.json())
            .then(json=>console.log(json))
</script>

<template>
    <div class="grid grid-col sm:grid sm:grid-cols-3 justify-items-center border border-black p-2 space-y-4">
        <!-- Instead of creating product items individually, figure out how to loop through them in accoradance to the api calls. -->
        <ProductItem class="mt-4">
            <template #image>
                <TheImage/>
            </template>
            <template #title>test title</template>
            <template #price>test price</template>
        </ProductItem>

        <ProductItem/>
        <ProductItem/>
        <ProductItem/>
        <ProductItem/>
        
    </div>
</template>