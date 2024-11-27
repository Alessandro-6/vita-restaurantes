<template>
  <ul class="flex space-x-2 capitalize text-slate-50">
    <li
      v-for="element in elements"
      :key="element"
      class="cursor-pointer py-2 px-4 rounded-full transition-all duration-500"
      :class="{ 'bg-[#222831]': active === element }"
      @click="setIsActive"
    >
      {{ element }}
    </li>
  </ul>
</template>

<script setup>
const { elements } = defineProps({
  elements: {
    type: Array,
    default: ["todos"],
  },
});

function setIsActive(e) {
  active.value = e.target.textContent;
}

const active = ref(elements[0]);
</script>
