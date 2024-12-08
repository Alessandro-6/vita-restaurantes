<template>
  <img
    :src="`/assets/${path}`"
    alt="burguer"
    class="border-8 w-96 h-96 object-cover border-transparent bg-gradient-to-tr from-yellow-500 to-orange-500 bg-clip-border hover:scale-105 duration-300 transition-all"
    :class="{ 'hover:rotate-6': right, 'hover:-rotate-6': !right }"
  />
</template>

<script setup>
defineProps({
  path: {
    type: String,
    default: "o1.jpg",
  },
  right: {
    type: Boolean,
    default: false,
  },
});
</script>
