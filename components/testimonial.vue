<script setup>
import { faStar } from "@fortawesome/free-solid-svg-icons";
</script>

<template>
  <div
    class="bg-[#222831] min-h-60 overflow-hidden duration-500 transition-all flex rounded-lg max-w-[30rem] -skew-x-6"
  >
    <div
      class="bg-slate-50 relative overflow-hidden flex justify-center items-center w-1/3 h-2/3 rounded-lg star-fade"
    >
      <img
        src="/public/assets/f1.png"
        alt="pizza"
        class="bg-cover transition-all duration-300 object-contain w-32 h-32"
      />
      <span
        class="absolute -bottom-8 text-emerald-800 text-xl inline-block transition-all duration-[.6s]"
        ><FontAwesome :icon="faStar" v-for="i in 5" :key="i" />
      </span>
    </div>
    <div class="w-2/3 h-full skew-x-6 py-6 px-10 text-justify">
      <Subtitle title="Alessandro Almeida" class="mb-5" />
      <p class="text-slate-50">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt iure,
        explicabo distinctio soluta numquam, ullam id minus rem esse obcaecati
        consequuntur.
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.star-fade {
  & * {
    transform: skewX(6deg) translateY(0);
  }
  &:hover img {
    filter: blur(0.25rem) grayscale(56%);
  }
  &:hover span {
    bottom: 50%;
    transform: skewX(-6deg) translateY(50%);
  }
}
</style>
