<script setup lang="ts">
import { ref } from 'vue'
import type { Ref } from 'vue'
import type { FormData } from '@/types/types';

const formData: Ref<FormData> = ref({
  name: '',
  email: '',
  phone: '',
  address: '',
  address2: '',
  city: '',
  state: '',
  zip: ''
})
const handleSubmit = (event: Event) => {
  event.preventDefault()
  const subEv = event as SubmitEvent
  console.log(subEv)
}
</script>

<template>
    <form @submit="handleSubmit" class="mt-4 max-w-5xl mx-auto">
      <div class="input-group inline-block w-1/2">
        <label for="name">Name</label>
        <input
          type="text"
          id="name"
          class="input"
          placeholder="enter name"
          v-model="formData.name"
        />
      </div>
      <div class="input-group w-1/2 inline-block">
        <label for="email">Email</label>
        <input
          type="email"
          id="email"
          class="input"
          placeholder="enter email"
          v-model="formData.email"
        />
      </div>

      <div class="input-group w-full">
        <label for="address">Address</label>
        <input
          type="text"
          id="address"
          class="input"
          placeholder="enter address"
          v-model="formData.address"
        />
      </div>
      <div class="input-group w-full">
        <label for="address2">Address 2</label>
        <input
          type="text"
          id="address2"
          class="input"
          placeholder="enter address 2"
          v-model="formData.address"
        />
      </div>
      <div class="input-group w-7/12 inline-block">
        <label for="city">City</label>
        <input
          type="text"
          id="city"
          class="input"
          placeholder="enter city"
          v-model="formData.city"
        />
      </div>
      <div class="input-group w-3/12 inline-block">
        <label for="state">State</label>
        <input
          type="text"
          id="state"
          class="input"
          placeholder="enter state"
          v-model="formData.state"
        />
      </div>
      <div class="input-group w-2/12 inline-block">
        <label for="zip">Zip</label>
        <input type="text" id="zip" class="input" placeholder="enter zip" v-model="formData.zip" />
      </div>
      <div class="text-end p-4">
        <button class="button" type="submit">Submit</button>
      </div>
    </form>
</template>
