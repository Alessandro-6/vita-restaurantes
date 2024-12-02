<template>
  <header
    class="grid grid-cols-12 items-center w-full from-[#222831] from-70% to-emerald-900 relative z-50 bg-gradient-to-r py-6 uppercase text-white font-medium max-h-36"
  >
    <nav class="flex justify-between col-start-2 items-center col-end-12">
      <NuxtLink to="/" class="flex items-center relative">
        <img
          src="/pizza-icon.png"
          alt="pizza-slice"
          class="absolute h-20 w-20 -left-8"
        />
        <Subtitle title="vita restaurantes" class="translate-x-12" />
      </NuxtLink>
      <ul class="flex space-x-4 items-center">
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
      <div class="flex space-x-4 items-center">
        <ul class="flex space-x-4">
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
        <BtnInline to="/order-online" link class="text-sm">
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
} from "@fortawesome/free-solid-svg-icons";
</script>
