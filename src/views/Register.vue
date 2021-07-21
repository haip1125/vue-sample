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
      <div class="flex items-center justify-between">
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
          @click="register"
        >
          Sign Up
        </button>
      </div>
    </form>
  </div>
</template>

<script lang="ts">
  import { ref, defineComponent } from 'vue'
  import firebase from 'firebase'
  import { useRouter } from 'vue-router' // import router

  export default defineComponent({
    name: 'Register',
    setup() {
      const email = ref('')
      const password = ref('')
      const router = useRouter() // get a reference to our vue router
      const register = () => {
        firebase
          .auth() // get the auth api
          .createUserWithEmailAndPassword(email.value, password.value) // need .value because ref()
          .then((data) => {
            console.log('Successfully registered!')
            router.push('/sign-in') // redirect to the feed
          })
          .catch((error) => {
            console.log(error.code)
            alert(error.message)
          })
      }
      return {
        register,
      }
    },
  })
</script>
