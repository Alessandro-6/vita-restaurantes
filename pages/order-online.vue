<template>
  <section class="grid grid-cols-12 py-24">
    <Newsletter class="col-start-2 h-[31rem] flex items-center col-end-12">
      <template #form>
        <Subtitle title="FAÇA UM PEDIDO" size="lg" class="mb-2" />
        <div class="flex items-center gap-10 justify-between w-full">
          <label for="name" class="font-semibold capitalize">nome:</label>
          <BookInput
            class="placeholder:text-slate-700 text-slate-950"
            type="text"
            name="name"
            id="name"
            placeholder="Primeiro Último"
          />
        </div>
        <div class="flex items-center gap-10 justify-between w-full">
          <label for="phone" class="font-semibold capitalize">telefone:</label>
          <BookInput
            class="placeholder:text-slate-700 text-slate-950"
            type="text"
            name="phone"
            id="phone"
            placeholder="+244 900 000 000"
          />
        </div>
        <div class="flex items-center gap-10 justify-between w-full">
          <label for="email" class="font-semibold capitalize">email:</label>
          <BookInput
            class="placeholder:text-slate-700 text-slate-950"
            type="text"
            name="email"
            id="email"
            placeholder="exemplo@exemplo.com"
          />
        </div>
        <div class="flex items-center justify-between w-full">
          <label for="people" class="font-semibold capitalize"> prato: </label>
          <BookInput
            class="placeholder:text-slate-700 text-slate-950"
            type="text"
            name="people"
            id="people"
            placeholder="Hamburguer vegano"
          />
        </div>
        <BtnInline type="submit" class="mt-4 w-full self-start"
          >fazer pedido</BtnInline
        >
      </template>
      <template #img>
        <img
          src="/public/assets/bg-hero-simple-pizza.png"
          alt="pizza on a table"
          class="h-full object-cover"
        />
      </template>
    </Newsletter>
  </section>
</template>

<script setup></script>
