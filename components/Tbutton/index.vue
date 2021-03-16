<template>
  <button :type="type" @click="$emit('onClick', $event)" class="bg-gradient-to-tr transform hover:scale-125 transition-transform duration-300 ease-in-out from-purple-600 via-pink-500 to-yellow-500 w-full py-2 px-4 rounded-md font-bold mx-2">
    <slot/>
  </button>
</template>
<script>
export default {
  props:{
    type: String
  }
}
</script>