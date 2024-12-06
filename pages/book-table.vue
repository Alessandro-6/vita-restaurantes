<template>
  <section class="py-20 grid grid-cols-12 gap-10">
    <div
      class="bg-[#222831] col-start-2 col-end-12 items-center text-white grid grid-cols-12 gap-10 rounded-md overflow-hidden"
    >
      <div class="col-start-1 col-span-6 pl-16">
        <Subtitle title="FAÇA UMA RESERVA" class="mb-6" />
        <BookForm />
      </div>
      <TheMap class="col-start-7 col-span-5 w-[32.3rem] rounded-lg h-full" />
    </div>
  </section>
</template>
