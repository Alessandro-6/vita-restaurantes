<template>
  <div
    class="flex bg-[#222831] text-white rounded-md justify-between overflow-hidden"
  >
    <form
      @submit.prevent
      class="flex gap-6 flex-col min-w-1/2 font-semibold px-12 justify-center"
    >
      <slot name="form" />
    </form>
    <div class="min-w-1/2 h-[35rem]">
      <slot name="img" />
    </div>
  </div>
</template>
