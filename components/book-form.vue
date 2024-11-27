<template>
  <form @submit.prevent class="flex gap-6 flex-col">
    <form-group>
      <label for="name" class="font-semibold capitalize">nome:</label>
      <BookInput
        type="text"
        name="name"
        id="name"
        placeholder="Primeiro Último"
      />
    </form-group>
    <form-group>
      <label for="phone" class="font-semibold capitalize">telefone:</label>
      <BookInput
        type="text"
        name="phone"
        id="phone"
        placeholder="+244 900 000 000"
      />
    </form-group>
    <form-group>
      <label for="email" class="font-semibold capitalize">email:</label>
      <BookInput
        type="text"
        name="email"
        id="email"
        placeholder="exemplo@exemplo.com"
      />
    </form-group>
    <form-group>
      <label for="people" class="font-semibold capitalize">
        quantas pessoas?
      </label>
      <BookInput type="number" name="people" id="people" placeholder="42" />
    </form-group>
    <form-group>
      <label for="date" class="font-semibold capitalize">reserva:</label>
      <BookInput type="date" name="date" id="date" class="text-slate-400" />
    </form-group>
    <BtnInline type="submit" class="self-start">BOOK NOW</BtnInline>
  </form>
</template>
