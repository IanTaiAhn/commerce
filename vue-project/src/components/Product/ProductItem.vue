<script setup>
console.log("in ProductItem")


</script>

<template>
    <div class="sm:w-[520px] sm:h-[700px] w-[280px] h-[420px] border border-black p-2 relative hover:cursor-pointer">
        <div class="flex flex-col justify-center gap-y-2 h-full p-2">
            <div class="p-2 max-w-full sm:max-h-[500px] max-h-[300px] flex justify-center">
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