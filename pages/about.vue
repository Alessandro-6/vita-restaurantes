<template>
  <section
    class="grid grid-cols-12 gap-10 py-24 bg-gradient-to-r from-cyan-950 to-green-900"
  >
    <div class="col-start-2 col-end-12 grid grid-cols-12 gap-10">
      <div class="col-start-2 col-span-5">
        <CtaImg path="burguer.jpg" />
      </div>
      <div
        class="col-start-7 col-span-6 flex gap-10 flex-col items-start text-white self-center"
      >
        <Subtitle title="Somos Vitasoft - Restaurantes" size="xl" />
        <p class="text-lg text-justify">
          Com o Vitasoft, você explora menus, faz encomendas para receber pratos
          deliciosos em casa ou reserva sua mesa com facilidade. Tudo o que você
          precisa está em um só lugar, sem complicações. Seja para um jantar
          especial ou para saborear sua comida favorita no conforto do lar,
          conte com a Vitasoft. Navegue, escolha e aproveite o melhor da
          gastronomia!
        </p>
        <BtnInline type="button" :text-white="false">Leia mais</BtnInline>
      </div>
    </div>
    <div class="col-start-2 col-end-12 grid grid-cols-12 gap-10">
      <div class="col-start-8 col-span-5">
        <CtaImg path="o2.jpg" right />
      </div>
      <div
        class="col-start-2 row-start-1 col-span-6 flex gap-10 flex-col items-start text-white self-center"
      >
        <Subtitle title="Nossa missão" size="xl" />
        <p class="text-lg text-justify">
          No Vita Restaurantes, nossa missão é oferecer serviços de qualidade
          que tornem sua experiência gastronômica simples e agradável.
          Priorizamos um atendimento excepcional para garantir que cada cliente
          se sinta valorizado e satisfeito. Mais do que entregar pratos ou
          reservar mesas, buscamos proporcionar confiança, praticidade e
          momentos especiais. Vita Restaurantes: qualidade e cuidado em cada
          detalhe!
        </p>
        <BtnInline type="button" :text-white="false">Leia mais</BtnInline>
      </div>
    </div>
    <div class="col-start-2 col-end-12 grid grid-cols-12 gap-10">
      <div class="col-start-2 col-span-5">
        <CtaImg path="beef.jpg" />
      </div>
      <div
        class="col-start-7 col-span-6 flex gap-10 flex-col items-start text-white self-center"
      >
        <Subtitle title="Visão - restaurantes" size="xl" />
        <p class="text-lg text-justify">
          Ser a principal plataforma gastronômica, reconhecida por conectar
          pessoas a experiências únicas com praticidade e qualidade. Queremos
          redefinir a forma como clientes interagem com restaurantes, sempre
          garantindo excelência e inovação. Vita Restaurantes: transformando
          cada refeição em uma experiência memorável!
        </p>
        <BtnInline type="button" :text-white="false">Leia mais</BtnInline>
      </div>
    </div>
  </section>
</template>
