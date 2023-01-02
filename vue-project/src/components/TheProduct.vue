<script>
export default {
  data() {
    return {
      title: "",
      price: 0,
      titleArr: ["title1", "title2", "title3", "title4", "title5"],
      priceArr: ["price1", "price2", "price3", "price4", "price5"],
      imgURL: "",
      img: {},
      productArr: []
    }
  },
  // `mounted` is a lifecycle hook which we will explain later
  mounted() {
    // Implement a loading screen while the api call is processing.

    fetch('https://fakestoreapi.com/products/2')
            .then(res=>res.json())
            .then((json=> {
                console.log(json);
                this.title = json.title;
                this.price = json.price;
                this.imgURL = json.image;
                // console.log(this.imgURL);
            }))

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
    import TheImage from './TheImage.vue';
</script>

<template>
    <div class="grid grid-col lg:grid lg:grid-cols-3 justify-items-center border border-black p-2 gap-4 -m-1">
        <ProductItem v-for="el in productArr">
          <template #image>
            <img class="max-w-full max-h-full" :src="el.image"/>
          </template>
          <template #title>{{ el.title }}</template>
          <template #price>${{ el.price }}</template>
        </ProductItem>
    </div>
</template>