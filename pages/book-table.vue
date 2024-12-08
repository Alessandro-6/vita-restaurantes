<template>
  <section class="py-20 grid grid-cols-12 gap-10">
    <div
      class="bg-[#222831] min-h-[33rem] col-start-2 col-end-12 items-center text-white flex justify-between rounded-md overflow-hidden"
    >
      <div class="flex flex-col px-16 min-w-[33rem]">
        <Subtitle title="FAÇA UMA RESERVA" size="lg" class="mb-6" />
        <BookForm />
      </div>
      <TheMap class="w-[34rem] h-full" />
    </div>
  </section>
</template>
