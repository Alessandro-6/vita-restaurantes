<template>
  <input
    :type="type"
    :name="name"
    :id="id"
    :placeholder="placeholder"
    class="py-2 book-input border placeholder:text-slate-400 border-gray-700 outline-none px-4"
    :class="{ 'w-full': size === 'full', 'min-w-72': size === 'normal' }"
  />
</template>

<style lang="scss" scoped>
.book-input {
  color: #020617;
  font-weight: 600;
}
</style>

<script setup>
defineProps({
  type: {
    type: String,
    default: "text",
  },
  name: { type: String, default: "" },
  id: { type: String, default: "" },
  placeholder: { type: String, default: "example" },
  size: { type: String, default: "normal" },
});
</script>
