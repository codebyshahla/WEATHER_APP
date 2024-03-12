<script setup>
import { ref } from 'vue'
const Email = ref('')
const Password = ref('')

const handleSubmit = () => {
  console.log('Form submitted!')
  console.log(Email.value, Password.value)
}
</script>

<template>
  <div class="flex items-center justify-center h-screen">
    <form @submit.prevent="handleSubmit" class="max-w-lg p-8 bg-white rounded-md shadow-md">
      <div>
        <h1 class="text-orange-500 text-2xl font-bold mb-6">
          Weather<span class="text-black">App</span>
        </h1>
      </div>

      <div class="mb-3 ">
        <label for="email" class="text-gray-700 font-normal">Email:</label>
        <input
          type="email"
          v-model="Email"
          required
          class="w-full p-1 border border-solid border-gray-300 rounded-md box-border outline-none"
          placeholder="Enter your Email"
        />
      </div>
      <div class="mb-3">
        <label for="password" class="text-gray-700 font-normal">Password:</label>
        <input
          type="password"
          v-model="Password"
          required
          class="w-full p-1 border border-solid border-gray-300 rounded-md box-border outline-none"
          placeholder="Enter your Password"
        />
      </div>

      <button
        type="submit"
        class="bg-orange-500 text-white p-1 rounded-md cursor-pointer transition duration-300 hover:bg-orange-700 w-full"
      >
        Log In
      </button>
      <p class="text-blue-500 mt-3">
        If you are not Sign Up?
        <router-link to="/">Sign up</router-link>
      </p>
    </form>
  </div>
</template>
