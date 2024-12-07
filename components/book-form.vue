<template>
  <form @submit.prevent class="flex gap-6 flex-col">
    <form-group class="space-x-12">
      <label for="name" class="font-semibold capitalize">nome:</label>
      <BookInput
        class="placeholder:font-semibold placeholder:text-slate-700"
        type="text"
        name="name"
        id="name"
        placeholder="Primeiro Último"
      />
    </form-group>
    <form-group class="space-x-12">
      <label for="phone" class="font-semibold capitalize">telefone:</label>
      <BookInput
        class="placeholder:font-semibold placeholder:text-slate-700"
        type="text"
        name="phone"
        id="phone"
        placeholder="+244 900 000 000"
      />
    </form-group>
    <form-group class="space-x-12">
      <label for="email" class="font-semibold capitalize">email:</label>
      <BookInput
        class="placeholder:font-semibold placeholder:text-slate-700"
        type="text"
        name="email"
        id="email"
        placeholder="exemplo@exemplo.com"
      />
    </form-group>
    <form-group class="space-x-12">
      <label for="people" class="font-semibold capitalize">
        quantas pessoas?
      </label>
      <BookInput
        class="placeholder:font-semibold placeholder:text-slate-700"
        type="number"
        name="people"
        id="people"
        placeholder="42"
      />
    </form-group>
    <form-group class="space-x-12">
      <label for="date" class="font-semibold capitalize">reserva:</label>
      <BookInput
        class="placeholder:font-semibold text-slate-700 font-semibold placeholder:text-slate-700"
        type="date"
        name="date"
        id="date"
      />
    </form-group>
    <BtnInline type="submit" class="w-full self-start">reservar</BtnInline>
  </form>
</template>
