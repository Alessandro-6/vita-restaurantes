<template>
  <section
    class="bg-gradient-to-r from-cyan-950 to-emerald-900 grid row-gap grid-cols-12"
  >
    <div
      class="col-span-10 col-start-2 min-h-screen items-center row-start-1 grid grid-cols-12 gap-10 py-24"
    >
      <div class="col-start-7 col-span-5">
        <CtaImg right />
      </div>
      <div class="col-start-2 flex flex-col gap-10 col-span-5 row-start-1">
        <Subtitle size="xl" title="vita restaurantes" />
        <p class="text-slate-50 text-lg text-justify">
          No Vita Restaurantes, você faz encomendas de pratos deliciosos ou
          reserva mesas de forma rápida e prática. Tudo em um só lugar, com
          poucos cliques. Esqueça complicações: navegue, escolha e aproveite o
          melhor da gastronomia. Vita Restaurantes, feito para você!
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
      <Subtitle title="nosso menu" size="xl" class="mb-4" />
      <div class="flex w-full flex-wrap justify-center gap-10">
        <Card
          v-for="dish in dishes"
          :path="dish.image"
          :key="dish.name"
          :title="dish.name"
          :price="dish.price"
          to="/order-online"
          :ingredients="dish.ingredients"
        >
          {{ dish.ingredients }}</Card
        >
      </div>
      <BtnInline to="/menu" link>explorar o menu</BtnInline>
    </div>
    <div
      class="grid grid-cols-12 col-start-2 col-span-10 flex-wrap justify-center min-h-screen"
    >
      <Subtitle
        title="Depoimentos dos clientes"
        size="xl"
        class="row-start-1 col-start-5 col-span-6 mb-4"
      />
      <Testimonial
        class="col-start-1 col-span-5 row-start-2 row-span-2"
        :right="true"
        :order="1"
        img="user-10.jpg"
        name="José Luís"
        testimonial="Encomendar pelo Vitasoft foi super rápido, e a comida chegou impecável. Adorei a experiência!"
      />
      <Testimonial
        class="col-start-8 col-span-5 row-start-3 row-span-2"
        :order="2"
        name="Eliúde Martins"
        img="user-11.jpg"
        testimonial="Fiz uma reserva para um jantar romântico e foi tudo perfeito. O site é muito prático e confiável!"
      />
    </div>
    <div class="col-start-2 flex justify-center col-end-12 pb-24">
      <Newsletter class="min-w-3/4">
        <template #form>
          <header class="text-justify">
            <Subtitle title="queres 25% de desconto?" size="xl" class="mb-6" />
            <p class="text-[.96rem] font-semibold">
              Gaste 25% a menos na sua primeira reserva se te subscreveres ainda
              hoje!
            </p>
          </header>

          <div class="flex flex-col gap-3 items-start justify-center w-full">
            <label for="email" class="font-semibold capitalize">email:</label>
            <BookInput
              type="text"
              name="email"
              id="email"
              placeholder="exemplo@exemplo.com"
              size="full"
              class="placeholder:font-semibold placeholder:text-slate-700 text-slate-950 font-semibold"
            />
          </div>
          <div class="flex flex-col gap-3 items-start justify-center w-full">
            <label for="phone" class="font-semibold capitalize"
              >telefone:</label
            >
            <BookInput
              type="text"
              name="phone"
              id="phone"
              placeholder="+244 900 000 000"
              size="full"
              class="placeholder:font-semibold placeholder:text-slate-700 text-slate-950 font-semibold"
            />
          </div>
          <BtnInline type="submit" class="self-start mt-4 w-full"
            >subscrever</BtnInline
          >
        </template>
        <template #img>
          <img
            src="/public/assets/bg-hero-pizza-table.png"
            alt="pizza on a table"
            class="h-full w-full object-cover"
          />
        </template>
      </Newsletter>
    </div>
  </section>
</template>

<style lang="scss" scoped></style>

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
    ingredients: [
      "Queijo mussarela",
      "Manjericão",
      "Azeitonas pretas",
      "Cogumelos",
      "Pepperoni",
      "Calabresa",
      "Frutos do mar",
      "Queijo parmesão",
    ],
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
]);
</script>
