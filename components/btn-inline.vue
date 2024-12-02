<template>
  <NuxtLink
    :to="to"
    class="bg-yellow-400 hover:shadow-lg hover:shadow-yellow-900 hover:-translate-y-[.15rem] active:shadow-md active:shadow-blue-950 active:translate-y-[.15rem] duration-300 transition-all uppercase inline-block font-semibold py-2 px-8 rounded-full"
    :class="{ 'text-white': textWhite, 'text-slate-950': !textWhite }"
    v-if="link"
  >
    <slot />
  </NuxtLink>
  <button
    v-else
    :type="type"
    class="bg-yellow-400 hover:shadow-lg hover:shadow-yellow-900 hover:-translate-y-[.15rem] active:shadow-md active:shadow-blue-950 active:translate-y-[.15rem] duration-300 transition-all py-2 uppercase inline-block font-semibold px-8 rounded-full"
    :class="{ 'text-white': textWhite, 'text-slate-950': !textWhite }"
  >
    <slot />
  </button>
</template>

<style></style>

<script setup>
defineProps({
  size: {
    type: String,
    default: "md",
  },
  textWhite: {
    type: Boolean,
    default: false,
  },
  type: {
    type: String,
    default: "button",
  },
  to: {
    type: String,
    default: "/",
  },
  link: {
    type: Boolean,
    default: false,
  },
});
</script>
