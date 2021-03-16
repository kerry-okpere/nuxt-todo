<template>
  <nav class="mx-10 md:mx-32 py-5 flex justify-between items-center">
    <div>
      <h1 class="text-lg font-extrabold capitalize">tsks</h1>
    </div>
    <div>
      <NuxtLink to="/login" class="py-2 px-5 hover:bg-gray-700 hover:border-gray-700 hover:border-2 rounded-md align-middle">Login</NuxtLink>
      <NuxtLink to="/login" class="py-2 px-4 border-gray-600 border-2 rounded-md align-middle">Sign up</NuxtLink>
    </div>
  </nav>
</template>
<script>
export default {
  
}
</script>