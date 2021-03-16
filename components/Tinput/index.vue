<template>
  <input @input="$emit('input', $event.target.value)" class="bg-transparent border-2 p-2 px-3 rounded-xl border-gray-800 w-full my-2" :placeholder="placeholder" :type="type"/>
</template>
<script>
export default {
  props:{
    placeholder: String,
    type:String
  },
  mounted(){
    console.log(this. placeholder)
  }
}
</script>