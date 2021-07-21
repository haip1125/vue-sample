<template>
  <div class="w-full max-w-xs">
    <form class="content-center mb-4 pb-8 pt-6 px-8 bg-white rounded shadow-md">
      <div class="mb-4">
        <label
          class="block mb-2 text-gray-700 text-sm font-bold"
          for="username"
        >
          Username
        </label>
        <input
          id="username"
          class="
            focus:shadow-outline
            px-3
            py-2
            w-full
            text-gray-700
            leading-tight
            border
            rounded
            focus:outline-none
            shadow
            appearance-none
          "
          type="text"
          placeholder="Username"
        />
      </div>
      <div class="mb-6">
        <label
          class="block mb-2 text-gray-700 text-sm font-bold"
          for="password"
        >
          Password
        </label>
        <input
          id="password"
          class="
            focus:shadow-outline
            px-3
            py-2
            w-full
            text-gray-700
            leading-tight
            border
            rounded
            focus:outline-none
            shadow
            appearance-none
          "
          type="password"
          placeholder="************"
        />
      </div>
      <div class="flex items-center justify-between mb-10">
        <button
          class="
            focus:shadow-outline
            px-4
            py-2
            w-full
            text-white
            font-bold
            bg-blue-500
            hover:bg-blue-700
            rounded
            focus:outline-none
          "
          @click="login"
        >
          Sign in
        </button>
      </div>
      <div class="flex items-center justify-between align-middle">
        <button
          class="
            focus:shadow-outline
            w-full
            text-white
            font-bold
            bg-blue-500
            hover:bg-blue-700
            rounded
            focus:outline-none
          "
          @click="signInWithGoogle"
        >
          <img
            class="float-left"
            src="../assets/btn_google_light_normal_ios.svg"
          />
          <div class="inline-block align-middle py-3">Sign in with Google</div>
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
      const login = () => {
        console.log('test')
      }
      const signInWithGoogle = () => {
        console.log('test2')
      }

      return {
        login,
        signInWithGoogle,
      }
    },
  })
</script>

<style scoped></style>
