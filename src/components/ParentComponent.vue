<script setup>
import {ref} from "vue";
import ChildComponent from "./ChildComponent.vue";

const message = ref("Hello World !! I am from parent components")

const messageReceivedFromChild = ref('')

function myAction(n) {
  messageReceivedFromChild.value = n
}

</script>

<template>

  <ChildComponent @message-Emitted="myAction" v-model:message="message"/>

  <div v-show="messageReceivedFromChild">
    <h1 class="text-black-900 text-xl my-5"><span class="text-green-500">
     Parent Component Received the message From Child Component through Emit :
       <span class="text-black font-bold">{{ messageReceivedFromChild }}
       </span>
     </span></h1>

  </div>

</template>

<style scoped>

</style>