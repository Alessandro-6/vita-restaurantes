<template>
  <footer
    class="pt-24 pb-16 bg-[#222831] font-medium from-sky-950 to-[#222831] bg-gradient-to-r text-white gap-6 grid grid-cols-12 to-25% w-full"
  >
    <div
      class="text-justify space-y-6 sm:space-y-0 flex flex-col items-center capitalize col-start-1 col-span-full sm:flex-row sm:col-start-2 sm:col-end-12 sm:justify-between"
    >
      <div class="relative flex flex-col items-center">
        <img
          src="/assets/about-pizza-img-1.png"
          alt="pizza-de-queijo"
          class="hidden sm:absolute sm:inline-block sm:-top-[11.5rem] sm:-left-28 w-48 h-48"
        />
        <Subtitle title="contacte-nos" class="mb-2" />
        <ul>
          <li>Avenida 21 de Janeiro, Luanda</li>
          <li>telefone +244 941 696 934</li>
          <li class="lowercase">propriedade0@gmail.com</li>
        </ul>
      </div>
      <div class="flex flex-col items-center sm:max-w-60">
        <Subtitle title="vita restaurantes" class="mb-2" />
        <p class="max-w-60">
          Entrega rápida e reservas fáceis para uma experiência saborosa!
        </p>
      </div>
      <div class="flex flex-col items-center">
        <Subtitle title="aberto" class="mb-2" />
        <p>todos os dias</p>
        <p>10:00H - 22:00H</p>
      </div>
    </div>
    <p
      class="row-start-2 col-start-2 sm:col-start-2 col-span-10 text-center sm:text-left sm:col-span-4"
    >
      &copy; 2024-2025 Vitasoft. Todos os direitos reservados
    </p>
    <ul
      class="row-start-3 sm:row-start-2 flex space-x-4 col-start-5 col-span-5 sm:col-start-10 fa-lg"
    >
      <li>
        <NuxtLink to="/">
          <font-awesome :icon="faFacebookSquare" class="text-blue-700" />
        </NuxtLink>
      </li>
      <li>
        <NuxtLink to="/">
          <font-awesome :icon="faInstagram" />
        </NuxtLink>
      </li>
      <li>
        <NuxtLink to="/">
          <font-awesome :icon="faYoutube" class="text-red-600" />
        </NuxtLink>
      </li>
    </ul>
  </footer>
</template>

<script setup>
import {
  faFacebookSquare,
  faInstagram,
  faYoutube,
} from "@fortawesome/free-brands-svg-icons";
</script>

<style scoped>
.gradient-text {
  background: linear-gradient(to right, red, yellow);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}
</style>
