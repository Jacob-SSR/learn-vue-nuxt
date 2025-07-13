<script setup>
import { ref } from "vue";

const childMessage = ref("Hello from parent");

const handleClick = () => {
  childMessage.value = "Hello from child";
};

const emit = defineEmits(["myEvent"]);

const handleClickFromParent = () => {
  emit("myEvent", "Hello from child");
};
</script>

<template>
  <h2>Parent Component</h2>
  <h1>{{ childMessage }}</h1>
  <button @click="handleClick">Cilck Me</button>
  <button @click="handleClickFromParent">Cilck me form parent</button>
  <slot name="myHeader">Default Header</slot>
</template>
