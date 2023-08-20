<script setup>
const props = defineProps(['message'])
const messageEmitted = defineEmits(['update:message'])

function showMessage() {
  props.name = messageEmitted('update:message', "This is the updated message clicked by the child component button")
}
</script>

<template>
  <h1 class="my-5">Props Received and Show the message:</h1>
  <br>
  <h2 class="text-black-900 text-xl my-5"><span class="text-red-600">{{ message }}</span></h2>
  <br>
  <br>
  <button @click="showMessage()" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">Click Me
  </button>
</template>

<style scoped>

</style>