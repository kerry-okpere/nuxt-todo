<template>
  <main class="min-h-screen text-white bg-gray-900 flex justify-center items-center text-center">
    <div>
      <div class="mb-10">
        <p class="text-3xl font-bold">
          <span v-if="this.auth === 'login'">Sign In.</span>
          <span v-else >Sign Up.</span>
        </p>
      </div>
      <p>or</p>
      <Authenticate :authOption="this.auth"/>     
    </div>

  </main>
</template>

<script>
  export default {
    async asyncData({ params }) {
      const auth = params.auth // When calling /abc the slug will be "abc"
      return { auth }
    },
  }
</script>