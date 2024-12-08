<script setup>
import { faStar } from "@fortawesome/free-solid-svg-icons";

defineProps({
  right: { type: Boolean, default: false },
  order: {
    type: Number,
    default: 1,
  },
  name: {
    type: String,
    default: "Alessandro Almeida",
  },
  img: {
    type: String,
    default: "f1.png",
  },
  testimonial: {
    type: String,
    default:
      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt iure, explicabo distinctio soluta numquam, ullam id minus rem esse obcaecati consequuntur.",
  },
});
</script>

<template>
  <div
    class="bg-[#222831] min-h-40 max-h-60 p-4 overflow-hidden duration-500 transition-all flex rounded-lg max-w-[30rem]"
    :class="{
      [`testimonial--${order}`]: true,
      '-skew-x-6': right,
      'skew-x-6': !right,
    }"
  >
    <div
      class="overflow-hidden border-4 border-slate-200 flex justify-center items-start w-36 h-36 rounded-full"
      :class="{
        '-skew-x-6': !right,
        'skew-x-6': right,
      }"
    >
      <img
        :src="`assets/${img}`"
        alt="pizza"
        class="transition-all duration-300 object-cover w-64 h-64"
      />
      <span
        class="absolute -bottom-8 text-emerald-800 opacity-50 text-lg inline-block transition-all duration-[.6s] scale-90"
        ><FontAwesome :icon="faStar" v-for="i in 5" :key="i" />
      </span>
    </div>
    <div
      class="w-2/3 h-full py-6 px-8 text-justify relative z-10"
      :class="{ '-skew-x-6': !right, 'skew-x-6': right }"
    >
      <Subtitle :title="name" class="mb-3" />
      <p class="text-slate-50 text-md font-semibold">
        {{ testimonial }}
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.star-fade {
  backface-visibility: hidden;
}
</style>
