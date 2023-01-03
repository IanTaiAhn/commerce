<script setup>
    import { RouterLink } from 'vue-router'
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
    <RouterLink :to=route class="hover:text-gray-300 group relative">
      {{ msg }}
      <span class="bg-black absolute left-0 -bottom-1 w-0 h-1 transition-all group-hover:w-full"></span>
    </RouterLink>
</template>