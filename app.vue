<template>
  <div
    class="overflow-x-hidden bg-blend-soft-light bg-gradient-to-r from-cyan-950 to-emerald-900"
  >
    <TheHeader />
    <NuxtPage />
    <TheFooter />
  </div>
</template>

<script setup>
useHead({
  htmlAttrs: {
    lang: "pt",
  },
  link: [
    {
      rel: "icon",
      type: "image/png",
      href: "/pizza-icon.png",
    },
  ],
});
</script>

<style>
.page-enter-active,
.page-leave-active {
  transition: all 0.2s;
}

.page-enter-from,
.page-leave-to {
  opacity: 0;
  filter: blur(0.5rem);
}

.page-enter-from {
  transform: translateX(-2rem) scale(98%);
}

.page-leave-to {
  transform: translateX(2rem) scale(98%);
}
</style>
