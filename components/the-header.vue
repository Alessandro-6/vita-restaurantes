<template>
  <header
    class="grid grid-cols-12 items-center w-full from-[#222831] from-70% to-emerald-900 relative z-50 bg-gradient-to-r py-6 uppercase text-white font-medium sm:max-h-36"
  >
    <nav
      class="flex flex-col sm:flex-row col-start-2 col-span-10 items-start justify-between sm:col-start-2 sm:items-center sm:col-end-12"
    >
      <NuxtLink to="/" class="flex items-center relative">
        <img
          src="/pizza-icon.png"
          alt="pizza-slice"
          class="absolute hidden sm:inline-block h-20 w-20 -left-8"
        />
        <Subtitle title="vita restaurantes" class="sm:translate-x-12" />
      </NuxtLink>

      <button
        class="sm:hidden hover:text-yellow-500 duration-200 transition-all self-end text-lg -translate-y-6"
        @click="setHidden"
      >
        <FontAwesome :icon="faList" />
      </button>

      <TransitionExpand>
        <ul
          class="sm:flex sm:space-x-4 items-center -translate-y-4 sm:-translate-y-0"
          v-if="hidden"
        >
          <NavLink class="hover:text-yellow-500 duration-300 transition-all">
            <NuxtLink
              to="/"
              active-class="bg-gradient-to-r from-yellow-400 to-orange-400 bg-clip-text text-transparent"
              >home</NuxtLink
            >
          </NavLink>
          <NavLink class="hover:text-yellow-500 duration-300 transition-all">
            <NuxtLink
              to="/about"
              active-class="bg-gradient-to-r from-yellow-400 to-orange-400 bg-clip-text text-transparent"
              >sobre</NuxtLink
            >
          </NavLink>
          <NavLink class="hover:text-yellow-500 duration-300 transition-all">
            <NuxtLink
              to="/menu"
              active-class="bg-gradient-to-r from-yellow-400 to-orange-400 bg-clip-text text-transparent"
              >menu</NuxtLink
            >
          </NavLink>
          <NavLink class="hover:text-yellow-500 duration-300 transition-all">
            <NuxtLink
              to="/book-table"
              active-class="bg-gradient-to-r from-yellow-400 to-orange-400 bg-clip-text text-transparent"
              >fazer-reserva</NuxtLink
            >
          </NavLink>
          <NavLink class="hover:text-yellow-500 duration-300 transition-all">
            <NuxtLink
              to="/testimonials"
              active-class="bg-gradient-to-r from-yellow-400 to-orange-400 bg-clip-text text-transparent"
              >depoimentos</NuxtLink
            >
          </NavLink>
        </ul>
      </TransitionExpand>
      <div class="flex sm:space-x-4 items-center">
        <ul class="sm:flex space-x-4 hidden">
          <NavLink>
            <NuxtLink to="#"> <FontAwesome :icon="faUser" /></NuxtLink>
          </NavLink>
          <NavLink>
            <NuxtLink to="#"><FontAwesome :icon="faShoppingCart" /></NuxtLink>
          </NavLink>
          <NavLink>
            <NuxtLink to="#"><FontAwesome :icon="faSearch" /></NuxtLink>
          </NavLink>
        </ul>
        <BtnInline
          to="/order-online"
          link
          class="text-sm hidden sm:inline-block"
        >
          fazer pedido
        </BtnInline>
      </div>
    </nav>
  </header>
</template>

<script setup>
import {
  faUser,
  faShoppingCart,
  faSearch,
  faList,
} from "@fortawesome/free-solid-svg-icons";

import { TransitionExpand } from "@morev/vue-transitions";
const hidden = ref(false);

function setHidden() {
  hidden.value = !hidden.value;
  console.log(hidden.value);
}
</script>
