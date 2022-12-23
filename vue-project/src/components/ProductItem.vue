<script setup>
defineProps({
  childImg: {
    type: String,
    required: true
  }
})
</script>

<template>
    <div class="w-64 h-72 border border-black p-2">
        <div class="flex flex-col justify-between h-full p-2">
            <!-- <p class="self-center"><slot name="image">null image</slot></p> -->
            <div class=" p-2">
                <img :src=childImg alt="test" class=""> 
            </div>
            <div class="flex flex-row justify-between">
                <h1 class=""><slot name="title">null title</slot></h1> 
                <h1 class=""><slot name="price">null price</slot></h1> 
            </div> 
        </div>
    </div>
</template>