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
    ingredients:
      "Molho de tomate, Mussarela, Camarões, siri, Lulas (em anéis), Cebola (em fatias finas) ",
    image: "f1.png",
  },
  {
    name: "hamburguer big",
    ingredients:
      "Pão com gergelim, Queijo cheddar, Beef patty, Cebola roxa, Tomate, Alface",
    image: "f2.png",
    price: 4500,
  },
  {
    name: "pizza de ortelã",
    ingredients:
      " Mussarela, queijo parmesão, tomate, cebola, manjericão, hortelã",
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
    name: "pizza mista",
    ingredients: "Queijo parmesão, tomate, cebola, orégano,",
    image: "f6.png",
  },
  {
    ingredients:
      " Pão com gergelim, Queijo cheddar, Tomate, Cebola, Filé, ovo, coentro",
    name: "hamburguer de peixe",
    image: "f7.png",
    price: 2700,
  },
  {
    name: "hamburguer vegano (sementes sésamo)",
    ingredients:
      "Pão com gergelim, Queijo cheddar, Tomate, Cebola, Filé, ovo, coentro, Alho picado,  tomate, alface",
    image: "f8.png",
    price: 3500,
  },
  {
    name: "lasanha",
    ingredients:
      " Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus, magnam neque possimus sequi aspernatur quis iste vel laudantium nesciunt, obcaecati voluptate. ",
    image: "f9.png",
  },
]);
</script>
