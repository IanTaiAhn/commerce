<script setup>
// defineProps({
//   childImg: {
//     type: String,
//     required: true
//   }
// })
</script>

<template>
    <div class="w-80 h-96 border border-black p-2">
        <div class="flex flex-col justify-between h-full p-2">
            <div class="p-2 w-9/12 self-center">
                <!-- <img :src=childImg alt="test" class="">  -->
                <slot name="image">
                    <img src="null"/>
                </slot>
            </div>
            <div class="flex flex-row justify-between">
                <h1 class=""><slot name="title">null title</slot></h1> 
                <h1 class=""><slot name="price">null price</slot></h1> 
            </div> 
        </div>
    </div>
</template>