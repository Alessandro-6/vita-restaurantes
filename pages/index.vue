<template>
  <section
    class="bg-gradient-to-r from-cyan-950 to-emerald-900 grid row-gap grid-cols-12 pb-24"
  >
    <div
      class="col-span-10 col-start-2 min-h-screen items-center grid grid-cols-12 gap-10 py-24"
    >
      <div class="col-start-7 col-span-5">
        <img
          src="/assets/o1.jpg"
          alt="burguer"
          class="border-8 border-transparent bg-gradient-to-tr from-yellow-500 to-orange-500 bg-clip-border hover:scale-105 duration-300 hover:rotate-6 transition-all"
        />
      </div>
      <div class="col-start-2 flex flex-col gap-10 col-span-5 row-start-1">
        <Subtitle size="xl" title="vita restaurantes"> </Subtitle>
        <p class="text-slate-50 text-lg text-justify">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatum,
          in itaque? Dolore pariatur dignissimos cumque recusandae consequuntur
          neque unde et similique itaque est, sed, aliquam hic cum voluptatem
          totam expedita! Lorem, ipsum dolor sit amet consectetur adipisicing
          elit. Esse temporibus fuga dolore iusto voluptatem rem, nostrum
          laboriosam explicabo et doloremque molestiae ut eveniet labore ipsa,
          placeat incidunt.
        </p>
        <BtnInline to="/book-table" link class="self-start">
          Fazer reserva
        </BtnInline>
      </div>
    </div>
    <div
      class="col-start-2 col-span-10 row-start-2 flex items-center justify-center gap-10"
    >
      <OnOffer
        img="lasanha.jpeg"
        title="Quinta da lasanha"
        :discount="25"
        class="w-1/2"
      />
      <OnOffer
        img="beef.jpg"
        title="fim de semana - churrasco"
        :discount="19"
        class="w-1/2"
      />
    </div>

    <div
      class="col-start-2 py-24 gap-10 col-span-10 row-start-3 flex flex-col items-center"
    >
      <Subtitle title="menu" size="xl" />
      <div class="flex w-full flex-wrap justify-center gap-10">
        <Card
          v-for="dish in dishes"
          :path="dish.image"
          :key="dish.name"
          :title="dish.name"
          :price="dish.price"
          to="/order-online"
        >
          {{ dish.ingredients }}</Card
        >
      </div>
      <BtnInline to="/menu" link>explorar o menu</BtnInline>
    </div>
  </section>
</template>

<style lang="scss" scoped></style>

<script setup>
const dishes = reactive([
  {
    name: "hamburguer big",
    ingredients:
      " Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus, magnam neque possimus sequi aspernatur quis iste vel laudantium nesciunt, obcaecati voluptate. ",
    image: "f2.png",
    price: 4500,
  },
  {
    name: "pizza de ortelã",
    ingredients:
      " Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus, magnam neque possimus sequi aspernatur quis iste vel laudantium nesciunt, obcaecati voluptate. ",
    image: "f3.png",
  },
  {
    name: "macarrão com estrogonofe",
    ingredients:
      " Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus, magnam neque possimus sequi aspernatur quis iste vel laudantium nesciunt, obcaecati voluptate. ",
    image: "f4.png",
  },
  {
    name: "batatas fritas",
    ingredients:
      " Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus, magnam neque possimus sequi aspernatur quis iste vel laudantium nesciunt, obcaecati voluptate. ",
    image: "f5.png",
  },
  {
    name: "hamburguer vegano",
    ingredients:
      " Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus, magnam neque possimus sequi aspernatur quis iste vel laudantium nesciunt, obcaecati voluptate. ",
    image: "f7.png",
    price: 2700,
  },
  {
    name: "lasanha",
    ingredients:
      " Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus, magnam neque possimus sequi aspernatur quis iste vel laudantium nesciunt, obcaecati voluptate. ",
    image: "f9.png",
  },
]);
</script>
