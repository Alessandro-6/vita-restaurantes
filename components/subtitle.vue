<template>
  <h3
    class="font-medium capitalize bg-gradient-to-r from-yellow-400 to-orange-500 to-75% bg-clip-text text-transparent"
    :class="{
      'text-xl': size !== 'lg' && size !== 'xl',
      'text-2xl': size === 'lg',
      'text-4xl': size === 'xl',
    }"
  >
    {{ title }}
  </h3>
</template>

<script setup>
defineProps(["title", "size"]);
</script>
