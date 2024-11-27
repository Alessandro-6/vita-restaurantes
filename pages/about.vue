<template>
  <section
    class="grid grid-cols-12 gap-10 py-24 bg-gradient-to-r from-sky-950 to-green-900"
  >
    <div class="col-start-2 col-span-5">
      <img src="/assets/about-pizza-img-1.png" alt="hamburguer" />
    </div>
    <div
      class="col-span-5 flex gap-10 flex-col items-start text-white self-center"
    >
      <Subtitle
        title="Somos VitaSoft - Restaurantes"
        size="xl"
        class="font-extralight"
      />
      <p class="text-lg">
        There are many variations of passages of Lorem Ipsum available, but the
        majority have suffered alteration in some form, by injected humour, or
        randomised words which don't look even slightly believable. If you are
        going to use a passage of Lorem Ipsum, you need to be sure there isn't
        anything embarrassing hidden in the middle of text. All
      </p>
      <BtnInline type="button" :text-white="false">Leia mais</BtnInline>
    </div>
  </section>
</template>
