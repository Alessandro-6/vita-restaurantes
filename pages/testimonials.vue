<template>
  <section
    class="bg-white pt-24 pb-28 grid grid-cols-12 bg-gradient-to-r from-cyan-950 to-green-900"
  >
    <div class="col-start-2 col-end-12 flex gap-10 items-center flex-col">
      <Subtitle title="depoimentos" size="xl" class="mb-6" />
      <div
        class="grid grid-cols-12 col-start-2 col-end-12 flex-wrap row-span-full justify-center col-span-6 min-h-screen"
      >
        <Testimonial
          class="col-start-1 col-span-5 row-start-1 row-span-2"
          :right="true"
          :order="1"
          testimonial="Adorei o Vitasoft! Fiz minha reserva com facilidade e tudo saiu perfeito."
        />
        <Testimonial
          class="col-start-8 col-span-5 row-start-2 row-span-2"
          :order="2"
          name="Ivandro Afonso"
          img="f3.png"
          testimonial="Comida excelente e entrega rápida. O site é muito prático!"
        />
        <Testimonial
          class="col-start-1 col-span-5 row-start-4 row-span-2"
          :right="true"
          :order="3"
          name="Mateus Cabingano"
          img="f8.png"
          testimonial="Reservei uma mesa em poucos cliques. Simples e eficiente!"
        />
        <Testimonial
          class="col-start-8 col-span-5 row-start-5 row-span-2"
          :order="4"
          name="Edson Francisco"
          img="f7.png"
          testimonial="Organizar um jantar especial nunca foi tão fácil. Recomendo o Vitasoft!"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
definePageMeta({
  pageTransition: {
    name: "close-in",
  },
});
</script>
