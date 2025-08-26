<script setup>
import Button from 'primevue/button'
import InputText from 'primevue/inputtext'
import { ref } from 'vue'

const formData = ref({
  email: '',
  password: '',
  firstname: '',
})
</script>

<template>
  <form>
    <div class="mb-3">
      <InputText
        name="email"
        type="text"
        placeholder="Введите email"
        v-model="formData.email"
        class="w-full"
      />
    </div>
    <div class="mb-3">
      <InputText
        name="password"
        type="password"
        placeholder="Введите пароль"
        v-model="formData.password"
        class="w-full"
      />
    </div>
    <div class="mb-3">
      <InputText
        name="firstname"
        type="text"
        placeholder="Введите свое имя"
        v-model="formData.firstname"
        class="w-full"
      />
    </div>
    <div class="grid grid-cols-2 gap-3">
      <Button type="submit" class="w-full" label="Вход" />
      <Button type="submit" icon="pi pi-github" class="w-full" label="GitHub" severity="contrast" />
    </div>
  </form>
</template>