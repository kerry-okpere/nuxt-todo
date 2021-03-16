<template>
  <form @submit.prevent="handleAuth" class="max-w-sm">
    <Tinput type="email" placeholder="Email" v-model="login.email"/>
    <Tinput type="password" placeholder="Password" v-model="login.password"/>
    <!-- Invalid Credentials -->
    <p v-if="error" class="text-red-700 w-7/12 mx-auto">We had issues validating your credentials, Please try again later</p>
    <div class="my-6">
      <Tbutton type="submit" v-if="this.authOption === 'login'" class="-mx-3">Sign Up</Tbutton> 
      <Tbutton type="submit" v-else class="-mx-3">Sign Up</Tbutton>
    </div>
    <div class="text-sm">
      <p class="my-2">Don't have an account? 
        <NuxtLink to="/login" class="font-bold"> Create an account</NuxtLink>
      </p>
      <NuxtLink to="/login" class="font-bold my-2"> Fogot Password</NuxtLink>
    </div>
  </form>
</template>
<script>
export default {
  props:{
    authOption: String
  },
  data() {
    return {
      login: {
        email: '',
        password: ''
      },
      error: null
    }
  },
  methods:{
    handleAuth(){
      try {
        // let response = await this.$auth.loginWith('local', { data: this.login })
        console.log(response)
      } catch (error) {
        this.error = error
        console.log(error)
      }
    }
  }
}
</script>