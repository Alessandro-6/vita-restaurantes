<template>
  <section
    class="grid grid-cols-12 py-24 bg-gradient-to-r from-cyan-950 to-green-900"
  >
    <div class="col-start-2 gap-10 col-span-10 flex flex-col items-center">
      <Subtitle title="Nosso Menu" size="xl" />
      <MenuFilter
        :elements="['todos', 'hamburguer', 'pizza', 'batatas-fritas']"
      />
      <div class="flex w-full flex-wrap justify-center gap-10">
        <Card
          v-for="dish in dishes"
          :path="dish.image"
          :key="dish.name"
          :title="dish.name"
          :price="dish.price"
          :ingredients="dish.ingredients"
        >
          {{ dish.ingredients }}</Card
        >
      </div>
      <BtnInline to="/" link>veja mais</BtnInline>
    </div>
  </section>
</template>

<script setup>
const dishes = reactive([
  {
    name: "pizza de queijo",
    ingredients: [
      "molho de tomate",
      "mussarela",
      "camarões",
      "siri",
      "lulas (em anéis)",
      "cebola (em fatias finas)",
    ],
    image: "f1.png",
  },
  {
    name: "hamburguer big",
    ingredients: [
      "pão com gergelim",
      "queijo cheddar",
      "beef patty",
      "cebola roxa",
      "tomate",
      "alface",
    ],
    image: "f2.png",
    price: 4500,
  },
  {
    name: "pizza de ortelã",
    ingredients: [
      "mussarela",
      "queijo parmesão",
      "tomate",
      "cebola",
      "manjericão",
      "hortelã",
    ],
    image: "f3.png",
  },

  {
    name: "pizza mista",
    ingredients: ["queijo parmesão", "tomate", "cebola", "orégano"],
    image: "f6.png",
  },
  {
    ingredients: [
      "pão com gergelim",
      "queijo cheddar",
      "tomate",
      "cebola",
      "filé",
      "ovo",
      "coentro",
    ],
    name: "hamburguer de peixe",
    image: "f7.png",
    price: 2700,
  },
  {
    name: "hamburguer vegano",
    ingredients: [
      "pão com gergelim",
      "queijo cheddar",
      "tomate",
      "cebola",
      "filé",
      "ovo",
      "coentro",
      "alface",
    ],
    image: "f8.png",
    price: 3500,
  },
  {
    name: "macarrão com estrogonofe",
    ingredients: [
      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus, magnam neque possimus sequi aspernatur quis iste vel laudantium nesciunt, obcaecati voluptate.",
    ],
    image: "f4.png",
  },
  {
    name: "batatas fritas",
    ingredients: [
      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus, magnam neque possimus sequi aspernatur quis iste vel laudantium nesciunt, obcaecati voluptate.",
    ],
    image: "f5.png",
  },
  {
    name: "lasanha",
    ingredients: [
      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus, magnam neque possimus sequi aspernatur quis iste vel laudantium nesciunt, obcaecati voluptate.",
    ],
    image: "f9.png",
  },
]);
</script>
