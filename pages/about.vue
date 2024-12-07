<template>
  <section
    class="grid grid-cols-12 gap-10 py-24 bg-gradient-to-r from-cyan-950 to-green-900"
  >
    <div class="col-start-2 col-span-5">
      <img src="/assets/about-pizza-img-1.png" alt="hamburguer" />
    </div>
    <div
      class="col-span-5 flex gap-10 flex-col items-start text-white self-center"
    >
      <Subtitle title="Somos Vitasoft - Restaurantes" size="xl" />
      <p class="text-lg text-justify">
        O Vitasoft é o seu parceiro para momentos gastronômicos incríveis. Aqui,
        você pode explorar menus variados, fazer encomendas para receber pratos
        quentinhos em casa ou reservar sua mesa no restaurante com facilidade.
        Nosso diferencial é a praticidade: tudo o que você precisa está em um só
        lugar. Esqueça complicações com vários aplicativos, no Vitasoft, tudo é
        rápido e descomplicado. Seja para um jantar especial no restaurante ou
        para aproveitar a melhor culinária no conforto do seu lar, o Vitasoft
        está aqui para você. Navegue, escolha e aproveite!
      </p>
      <BtnInline type="button" :text-white="false">Leia mais</BtnInline>
    </div>
  </section>
</template>
