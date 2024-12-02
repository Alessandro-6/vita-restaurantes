<template>
  <div class="bg-[#222831] flex items-center rounded-md min-h-52 min-w-96">
    <div class="w-5/12 h-full ml-6">
      <img
        :src="`/assets/${img}`"
        class="h-44 w-44 object-cover border-4 bg-gradient-to-r from-yellow-500 to-orange-500 bg-clip-border border-transparent rounded-full"
        alt="food-img"
      />
    </div>
    <div class="flex flex-col gap-2 items-start">
      <Subtitle :title="title" />
      <span class="text-white text-xl mb-4">
        <span class="text-5xl">{{ discount }}%</span>
        <span class="font-thin text-2xl"> de desconto</span>
      </span>
      <BtnInline to="/order-online" link
        >Fazer pedido <FontAwesome :icon="faCartShopping"
      /></BtnInline>
    </div>
  </div>
</template>

<script setup>
import { faCartShopping } from "@fortawesome/free-solid-svg-icons";

defineProps({
  img: {
    type: String,
    default: "f2.png",
  },
  discount: {
    type: Number,
    default: 10,
  },
  title: {
    type: String,
    default: "burguer",
  },
});
</script>
