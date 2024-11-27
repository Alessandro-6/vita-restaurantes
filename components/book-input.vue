<template>
  <input
    :type="type"
    :name="name"
    :id="id"
    :placeholder="placeholder"
    class="min-w-72 py-2 border placeholder:text-slate-400 border-gray-700 outline-none px-4"
  />
</template>

<script setup>
defineProps(["type", "name", "id", "placeholder"]);
</script>
