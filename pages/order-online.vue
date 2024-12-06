<template>
  <section class="grid grid-cols-12 py-24">
    <Newsletter class="col-start-2 col-end-12">
      <template #form>
        <Subtitle title="FAÇA UM PEDIDO" size="lg" class="mb-4" />
        <form-group class="min-w-[24.6rem]">
          <label for="name" class="font-semibold capitalize">nome:</label>
          <BookInput
            class="placeholder:text-slate-700 text-slate-950"
            type="text"
            name="name"
            id="name"
            placeholder="Primeiro Último"
          />
        </form-group>
        <form-group class="min-w-[24.6rem]">
          <label for="phone" class="font-semibold capitalize">telefone:</label>
          <BookInput
            class="placeholder:text-slate-700 text-slate-950"
            type="text"
            name="phone"
            id="phone"
            placeholder="+244 900 000 000"
          />
        </form-group>
        <form-group class="min-w-[24.6rem]">
          <label for="email" class="font-semibold capitalize">email:</label>
          <BookInput
            class="placeholder:text-slate-700 text-slate-950"
            type="text"
            name="email"
            id="email"
            placeholder="exemplo@exemplo.com"
          />
        </form-group>
        <form-group class="min-w-[24.6rem]">
          <label for="people" class="font-semibold capitalize"> prato: </label>
          <BookInput
            class="placeholder:text-slate-700 text-slate-950"
            type="text"
            name="people"
            id="people"
            placeholder="Hamburguer vegano"
          />
        </form-group>
        <BtnInline type="submit" class="mt-4 w-full self-start"
          >reservar</BtnInline
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
