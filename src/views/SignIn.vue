<template>
  <div class="w-full max-w-xs">
  <form class="bg-white shadow-md rounded px-8 pt-6 pb-8 mb-4 content-center">
    <div class="mb-4">
      <label class="block text-gray-700 text-sm font-bold mb-2" for="username">
        Username
      </label>
      <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="Username">
    </div>
    <div class="mb-6">
      <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
        Password
      </label>
      <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="password" type="password" placeholder="******************">
    </div>
    <div class="flex items-center justify-between mb-10">
      <button class="w-full bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline" @click="login">
        Sign in
      </button>
    </div>
    <div class="flex items-center justify-between align-middle">
      <button class="w-full bg-blue-500 hover:bg-blue-700 text-white font-bold rounded focus:outline-none focus:shadow-outline" @click="login">
        <img class="float-left" src="../assets/btn_google_light_normal_ios.svg" /><div class="inline-block align-middle py-3">Sign in with Google</div>
      </button>
    </div>
  </form>
</div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
export default defineComponent({
  name: 'SignIn',
  setup: () => {
  },
  methods: {
    login() {
      console.log('test');
    },
    singnInWithGoogle() {
      console.log('test2'); 
    }
  }
})
</script>

<style scoped>

</style>
