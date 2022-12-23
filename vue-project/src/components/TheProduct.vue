<script>
export default {
  data() {
    return {
      title: "",
      price: 0,
      titleArr: ["title1", "title2", "title3", "title4", "title5"],
      priceArr: ["price1", "price2", "price3", "price4", "price5"],
      imgURL: "",
      img: {}
    }
  },
  // `mounted` is a lifecycle hook which we will explain later
  mounted() {
    // fetch('https://fakestoreapi.com/products/1')
    //         .then((res=>{
    //             res
    //         }))
    fetch('https://fakestoreapi.com/products/1')
            .then(res=>res.json())
            .then((json=> {
                console.log(json);
                this.title = json.title;
                this.price = json.price;
                this.imgURL = json.image;
                console.log(this.imgURL);
            }))
  }

}
</script>
<script setup>
    import ProductItem from './ProductItem.vue';
    import TheImage from './TheImage.vue';
    let testString = "hooby";
</script>

<template>
    <div class="grid grid-col sm:grid sm:grid-cols-3 justify-items-center border border-black p-2 space-y-4">
        <ProductItem class="mt-4" :childImg="imgURL">
            <template #title>{{ title }}</template>
            <template #price>${{ price }}</template>
        </ProductItem>
        <ProductItem/>
        <ProductItem/>
        <ProductItem/>
        <ProductItem/>
        <!-- <img src={{ img }} alt=""> -->
        <!-- Ideally I loop through the product items, and we only fetch data here. -->
        <!-- <img src="https://fakestoreapi.com/img/81fPKd-2AYL._AC_SL1500_.jpg" alt=""> -->
    </div>
</template>