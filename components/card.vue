<template>
  <div class="min-h-[28rem] card w-72">
    <div
      class="card__front h-full w-full shadow-xl rounded-md overflow-hidden shadow-emerald-950"
    >
      <div class="bg-slate-100 h-2/5 items-center flex justify-center">
        <img
          :src="`/assets/${path}`"
          class="h-36 w-36 object-contain"
          :alt="title"
        />
      </div>
      <div class="bg-[#222831] text-slate-50 p-6 h-3/5">
        <h2 class="capitalize font-medium text-xl mb-4">{{ title }}</h2>
        <p>
          <slot />
        </p>
      </div>
    </div>
    <div
      class="card__back h-full w-full rounded-md shadow-xl overflow-hidden p-6 shadow-emerald-950 flex flex-col gap-32 items-center justify-center bg-gradient-to-tr to-emerald-800 from-blue-950"
    >
      <h3
        class="font-thin text-6xl bg-gradient-to-r from-yellow-400 to-orange-500 bg-clip-text text-transparent"
      >
        {{ price }}Kz
      </h3>
      <btn-inline :to="to" link type="button">
        <span
          class="inline-block bg-gradient-to-r to-red-600 from-orange-700 bg-clip-text text-transparent"
        >
          Encomendar
        </span>
      </btn-inline>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  position: relative;
  perspective: 100rem;
  & > * {
    backface-visibility: hidden;
    transition: all 1.2s cubic-bezier(0.4, 0, 0.2, 1);
  }
  &:hover &__back {
    transform: rotateY(0deg);
  }
  &:hover &__front {
    transform: rotateY(180deg);
  }
  &__back {
    position: absolute;
    color: white;
    transform: rotateY(-180deg);
  }
  &__front {
    position: absolute;
    z-index: 10;
  }
}
</style>

<script setup>
const { path } = defineProps({
  path: {
    type: String,
    default: "",
  },
  title: {
    type: String,
    default: "",
  },
  price: {
    type: Number,
    default: 5000,
  },
  to: {
    type: String,
    default: "/",
  },
});
</script>
