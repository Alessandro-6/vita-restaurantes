<template>
  <div
    class="bg-blend-soft-light bg-gradient-to-r from-blue-950 to-emerald-900"
  >
    <TheHeader />
    <NuxtPage class="min-h-screen" />
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
  transition: all 0.45s;
}

.page-enter-from,
.page-leave-to {
  opacity: 0;
  filter: blur(0.5rem);
}

.page-enter-from {
  transform: translateX(-6rem);
}

.page-leave-to {
  transform: translateX(6rem);
}
</style>
