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
        // console.log(json);
        this.productArr = json;
    }))
  },
  methods: {
    someEventParent(event) {
      console.log("event fired from parent");
      console.log(event);
      // console.log("whut");
    }
  }
}
</script>
<script setup>
    import ProductItem from './ProductItem.vue';
</script>

<template>
    <div class="grid grid-col 2xl:grid 2xl:grid-cols-3 justify-items-center p-2 gap-4 mt-4 w-full">
        <ProductItem 
          v-for="el in productArr"
          :key="el.id"
          @someEvent="someEventParent"
        >
          <template #image >
            <img class="max-w-full max-h-full"
            :src="el.image"
          />
          </template>
          <template #title>{{ el.title }}</template>
          <template #price>${{ el.price }}</template>
        </ProductItem>
    </div>
</template>