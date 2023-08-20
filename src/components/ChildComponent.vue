<script setup>
defineProps(['message'])
defineEmits(['messageEmitted'])

</script>

<template>
  <h1 class="text-black-900 text-xl my-5"><span class="text-red-600">Child Component Received the message through Props : <span
      class="text-green-600">{{ message }}</span>  </span></h1>

  <button @click="$emit('messageEmitted', 'Hello World !!!! I am from Child components')"
          class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">Click Me
  </button>
</template>

<style scoped>

</style>