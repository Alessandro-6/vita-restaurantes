<template>
  <footer
    class="pt-24 pb-16 bg-[#222831] from-sky-950 to-[#222831] bg-gradient-to-r text-white gap-6 grid grid-cols-12 to-25% w-full"
  >
    <div class="capitalize col-start-2 col-end-12 flex justify-between">
      <div class="relative">
        <img
          src="/assets/about-pizza-img-1.png"
          alt="pizza-de-queijo"
          class="absolute -top-[11.5rem] -left-28 w-48 h-48"
        />
        <Subtitle title="contacte-nos" class="mb-2" />
        <ul>
          <li>Avenida 21 de Janeiro, Luanda</li>
          <li>telefone +244 941 696 934</li>
          <li>propriedade0@gmail.com</li>
        </ul>
      </div>
      <div class="max-w-60">
        <Subtitle title="vita restaurantes" class="mb-2" />
        <p>
          Necessary, making this the first true generator on the Internet. It
          uses a dictionary of over 200 Latin words, combined with
        </p>
      </div>
      <div>
        <Subtitle title="aberto:" class="mb-2" />
        <p>todos os dias</p>
        <p>10:00H - 22:00H</p>
      </div>
    </div>
    <p class="row-start-2 col-start-2 col-span-4">
      &copy; 2024-2025 VitaSoft. Todos os direitos reservados
    </p>
    <ul class="row-start-2 flex space-x-6 col-start-10 fa-lg">
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
