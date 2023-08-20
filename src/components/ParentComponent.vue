<script setup>
import {ref} from "vue";
import ChildComponent from "./ChildComponent.vue";

const message = ref("Hello World")

</script>

<template>
  <ChildComponent v-model:message="message"/>
</template>

<style scoped>

</style>