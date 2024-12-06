<template>
  <div class="flex bg-[#222831] text-white rounded-md overflow-hidden">
    <form
      @submit.prevent
      class="flex gap-6 flex-col min-w-[30rem] font-semibold px-16 justify-center"
    >
      <slot name="form" />
    </form>
    <div class="min-w-[35rem] h-[35rem]">
      <slot name="img" />
    </div>
  </div>
</template>
