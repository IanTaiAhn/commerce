<script>
export default {
  data() {
    return {
      title: "",
      price: 0
    }
  },
  // `mounted` is a lifecycle hook which we will explain later
  mounted() {
    fetch('https://fakestoreapi.com/products')
            .then(res=>res.json())
            .then((json=> {
                console.log(json);
                this.title = json.title;
                this.price = json.price;
            }))
  }
}
</script>
<script setup>
    import ProductItem from './ProductItem.vue';
    import TheImage from './TheImage.vue';
</script>

<template>
    <div class="grid grid-col sm:grid sm:grid-cols-3 justify-items-center border border-black p-2 space-y-4">
        <ProductItem class="mt-4">
            <template #image>
                <TheImage/>
            </template>
            <template #title>{{ title }}</template>
            <template #price>${{ price }}</template>
        </ProductItem>

        <ProductItem/>
        <ProductItem/>
        <ProductItem/>
        <ProductItem/>
        
    </div>
</template>