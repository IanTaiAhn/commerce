<script setup>
defineProps({
  route: {
    type: String,
    required: true
  },
  msg: {
    type: String,
    required: true
  }
})
</script>


<template>
    <a :href=route class="hover:text-purple-300 group relative">
        {{ msg }}
        <span class="bg-yellow-300 absolute left-0 -bottom-1 w-0 h-1 transition-all group-hover:w-full"></span>
    </a>
</template>