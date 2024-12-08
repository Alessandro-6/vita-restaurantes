<template>
  <div
    class="flex bg-[#222831] text-white rounded-md justify-center overflow-hidden"
  >
    <form
      @submit.prevent
      class="flex gap-6 flex-col min-w-[33rem] font-semibold px-16 justify-center"
    >
      <slot name="form" />
    </form>
    <div class="min-w-1/2 h-[35rem] ml-auto">
      <slot name="img" />
    </div>
  </div>
</template>
