<template>
  <header
    class="grid grid-cols-12 items-center w-full from-[#222831] from-70% to-emerald-900 bg-gradient-to-r py-6 uppercase text-white font-medium max-h-36"
  >
    <nav class="flex justify-between col-start-2 items-center col-end-12">
      <NuxtLink to="/" class="flex items-center relative">
        <img
          src="/pizza-icon.png"
          alt="pizza-slice"
          class="absolute h-20 w-20 -left-6"
        />
        <Subtitle title="vita restaurantes" class="translate-x-16" />
      </NuxtLink>
      <ul class="flex space-x-4 items-center">
        <li><NuxtLink to="/">home</NuxtLink></li>
        <li><NuxtLink to="/about">sobre</NuxtLink></li>
        <li><NuxtLink to="/menu">menu</NuxtLink></li>
        <li><NuxtLink to="/book-table">fazer-reserva</NuxtLink></li>
      </ul>
      <div class="flex space-x-4 items-center">
        <ul class="flex space-x-4">
          <li>
            <NuxtLink to="/"> <FontAwesome :icon="faUser" /></NuxtLink>
          </li>
          <li>
            <NuxtLink to="/"><FontAwesome :icon="faShoppingCart" /></NuxtLink>
          </li>
          <li>
            <NuxtLink to="/"><FontAwesome :icon="faSearch" /></NuxtLink>
          </li>
        </ul>
        <BtnInline to="/" text-white link>fazer pedido</BtnInline>
      </div>
    </nav>
  </header>
</template>

<script setup>
import {
  faUser,
  faShoppingCart,
  faSearch,
} from "@fortawesome/free-solid-svg-icons";
</script>
