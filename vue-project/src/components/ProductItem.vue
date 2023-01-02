<script setup>
// defineProps({
//   childImg: {
//     type: String,
//     required: true
//   }
// })
</script>

<template>
    <div class="w-80 h-96 border border-black p-2 relative">
        <div class="flex flex-col justify-center gap-y-8 h-full p-2">
            <div class="p-2 max-h-64 flex justify-center">
                <slot class="" name="image"></slot>
            </div>
        </div>
        <div class="absolute bottom-0 left-0 w-full p-2">
            <div class="flex flex-row justify-between w-full p-2">
                <h1 class="truncate"><slot name="title">null title</slot></h1> 
                <h1 class=""><slot name="price">null price</slot></h1> 
            </div> 
        </div>
    </div>
</template>