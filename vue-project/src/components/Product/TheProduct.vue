<script>
export default {
  data() {
    return {
      productArr: []
    }
  },
  mounted() {
    // Implement a loading screen while the api call is processing.
    fetch('https://fakestoreapi.com/products')
    .then(res=>res.json())
    .then((json=> {
        console.log(json);
        this.productArr = json;
    }))
  }
}
</script>
<script setup>
    import ProductItem from './ProductItem.vue';
</script>

<template>
    <div class="grid grid-col lg:grid lg:grid-cols-3 justify-items-center border border-black p-2 gap-4 -m-1 mt-4">
        <ProductItem v-for="el in productArr" :key="el.id">
          <template #image>
            <img class="max-w-full max-h-full" :src="el.image"/>
          </template>
          <template #title>{{ el.title }}</template>
          <template #price>${{ el.price }}</template>
        </ProductItem>
    </div>
</template>